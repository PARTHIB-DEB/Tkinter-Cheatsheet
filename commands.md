
Its a simple cheatsheet of Tkinter by which we can create desktop GUI by Python


## Commands

```bash
  from tkinter import *
```
To initiliaze a project , first of all we have to initialize a window - 

```bash
  root=Tk()
```
Everything in Tkinter is a *widget* , so a command to create a widget

```bash
  wd=label(root,text="....",params)
```

To give a title on window
```bash
    root.title("....")
```
**Important params of widgets**

| Params  | What it does |
| ------------- | ------------- |
| text  | shows a text/headline  |
| bd/background  | some color on background  |
| fg/foreground  | some color on foreground  |
| font  | font-name size type  |
| padx | padding in X  |
| pady | padding in Y  |
| relief | Border style  |

**In Tkinter , we have to bundle everything to main window**

```bash
  wd.pack(anchor="....",fill=X or Y,side=left or right or top )
```
*Gneral paramters in pack*

To shape the window , we use *geometry* widget (*W*-width , *H*-Height), It's the default screensize when we run the file

```bash
  root.geometry("WxH")
```
To give the window a minimum and maximum expandable size

```bash
   root.maxsize(W,H)
   root.minsize(W,H)
```

To put an image in our window , we use *PhotoImage* widget

To display the image we have to use the *lable* widget , basically label gives a particular identity to each individual widget, but it is not interactive

```bash
    wd=PhotoImage(file="abc.ext")
    label_wd=label(image=wd)
    label_wd.pack()
```

**OR**

To support any unsupported images , install *pillow*

```bash
    from PIL import Image,ImageTk
    image=Image.open(file="abc.ext")
    photo=ImageTk.PhotoImage(image)
```

To set block wise componental UI , We use *Frame*

```bash
  f=Frame(root,bg="color_name",borderwidth=numeric)
```

**Looping the changes in Main window and restart**

```bash
  root.mainloop()
```
