
Its a simple cheatsheet of Tkinter by which we can create desktop GUI by Python


## Commands

```bash
  from tkinter import *
```
To initiliaze a project , first of all we have to initialize a window - 
A typical Tkinter window is basically an object of *TK* class

```bash
  root=Tk()
```

To give a title on window
```bash
    root.title("....")
```

Everything in Tkinter is a *widget* , so a command to create a widget named *label*

```bash
  wd=label(root,text="....",params)
```

**General parameters of every widget**

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
  wd.pack(anchor="....",fill=X or Y,side=left or right or top)
```
*General paramters in pack*

To shape the window , we use *geometry* widget (*W*-width(numeric) , *H*-Height(numeric)), It's the default screensize when we run the file

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

To use buttons, we have to to declare a frame atleast, inside a frame we can put several buttons

```bash
  def function_name():
    pass
  bt=Button(f,fg="",text="",commands=function_name)
```

In grid format , we can specify location of block components (*label*, *frame*,*image*,*buttons*,*entry* etc),To initialize a grid structure (comrpise of ROWS and COLUMNS)


```bash
  x=some kinds of widgets
  x.grid(row=num,
  col=num)
```

To Get user input there are 4 datatypes

```bash
  Valuetype=StringVar()
  or
  Valuetype=DoubleVar()
  or
  Valuetype=IntVar()
  or
  Valuetype=BooleanVar()

  value=Entry(root,textVariable=Valuetype)
```

For checkbuttons , we use *CheckButtons*

```bash
  k=CheckButton(text="",variable= Valuetype)
```

##

**Looping the changes in Main window and restart**

```bash
  root.mainloop()
```
