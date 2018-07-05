![Logo](https://raw.githubusercontent.com/sawyersteven/chromaprint/master/img/Logo_wide.png)

# chromaprint
Python module to facilitate effortless color terminal output.

### Installation
Chromaprint requires Python 3.X.

Install via pip with `pip install chromaprint`


### Usage
    from chromaprint import print
    print('green on magenta', fg='green', bg='magenta')

It's that easy.

Chromaprint contains one property `colors` and two methods `print` and `set_default`.

##### colors
`chromaprint.colors` is a tuple containing the names of all available colors. Attempts to use colors not in this tuple will raise an exception.

##### print()
The `print()` method functions the same as Python's built-in print method. Simply pass any strings you wish to print with the foreground color as `fg='green'` and background color as `bg='magenta'`. Color selections only apply to a single print, so the next `print` call will use the default colors. You can change the default colors using `chromaprint.set_default()`

##### set_default()
A custom set of default colors may be specified and changed at will. Simply call `set_default()` using the same syntax as `chromaprint.print()`, ie `chromaprint.set_default(bg='green', fg='magenta')`. You may set either `bg`, `fg`, or both. To return to the system default color output pass `bg='default', fg='default'`
