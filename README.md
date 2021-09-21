# Marquee
The best text to rolling text gif creator!
## Getting started

Download this project by clicking on download, or clone it!
```
git clone https://github.com/HerrLantz/marquee
```

### Prerequisites

**Marquee** requires [ImageMagick](https://www.imagemagick.org/script/index.php) and [Gifsicle](http://www.lcdf.org/gifsicle/)!

Install ImageMagick on Mac with homebrew:
```bash
brew install imagemagick
```
Install Gifsicle on Mac with homebrew:
```bash
brew install gifsicle
```

Install on debian-based linux distributions:
```
sudo apt-get update
sudo apt-get install imagemagick
sudo apt-get install gifsicle
```

After you have installed imagemagick, gifsicle and downloaded **Marquee**; then put the **Marquee** in some directory.
Export the **Marquee** directory path to your $PATH by:
```bash
export PATH=$PATH:/path/to/marquee
```
or you can add that line to your *.bash_profile* or wherever you want to export your $PATH.

Micke, you should change the file mode on *marquee* by
```bash
chmod 755 marquee
```


## Examples

```
marquee "Marquee is the best program ever" -background-color none -text-color magenta
```
![A great example](https://raw.githubusercontent.com/HerrLantz/marquee/master/examples/example1.gif "Look at that nice text")

```
marquee "Color blind people are superior" -b yellow -c brown
```
![Another great example](https://raw.githubusercontent.com/HerrLantz/marquee/master/examples/example2.gif "I wish I was like Patric")

```
marquee "Seizure inducing GIFs\!" -b rainbow -c rainbow
```
![An even greater example](https://raw.githubusercontent.com/HerrLantz/marquee/master/examples/example3.gif "Trippy!")
## Creating marquee gifs
To run **Marquee** simply type `marquee [text] [OPTIONS]` in the terminal.
If you are having trouble running **Marquee**, type `marquee -help` or `marquee -h` to get various help.


Here are all the different flags that can be used! Look how nice they are.

|Flag	             |Parameter	      |Effect                               |
|:-------------------|:--------------:|------------------------------------:|
|-name/-n            |.+\\.gif        |The name of the outputed gif         |
|-text-color/-c.     |name of a color |Sets the text color 		            |
|-background-color/-b|name of a color |Sets the background color            |
|-help/-h            |no parameter    |Gives help to slow people            |
|-delay/-d 			 |Positiv integer |Sets the delay between frames        |
|-font/-t            |Name of font    |Sets the font on the text            |
|-frames/-f          |Positiv integer |Depricated, does nothing             |
|-optimization/-o    |0, 1, 2 or 3    |Optimizes the file size (lossy)      |
|-list-fonts/-lf     |no parameter    |Lists all possible fonts             |
|-gaussian-blur/-gs  |[0-9]+x[0-9]+   |Blur each frame of the gif           |
|-swirl/-s           |Integer         |Swirl each frame by the given degree | 

## Windows

I don't like Windows, so the script won't generate a gif on that platform. Instead it creates a bunch of files with *Meow* in it.
