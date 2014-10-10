pythonjs
========

This is a *very basic* Python->JavaScript translator written in Python. This translator will convert relatively simple Python/NumPy functions to JavaScript, using our [numpy.js](https://github.com/vispy/numpy.js). Typically, these functions will be interactivity functions (like callback functions reacting to mouse movements, key strokes...) and emitting GLIR (OpenGL) commands to update the visualization.

We'll start from PythonJS and Pythonium code. We'll only support the most common Python/NumPy syntactic constructs. The code of these projects is based on the Python `ast` module. They generate JavaScript code dynamically while visiting the Python AST.

* `for` loops
* `if`
* NumPy indexing (converted to `get` and `set` in numpy.js)
* function calls and definitions
* tuples and lists converted to arrays

Vispy-specific features:

* Vispy gloo commands will be translated to vispy.gloo.js calls
* There should be a global symbol table that is used to access gloo objects in both Python and JavaScript


## Features not implemented

These features won't be implemented, at least in a first approach. The idea is to only support numerical computing functions relying on the `ndarray` structure.

* Classes
* Dynamic features (`getattr` and co)
* Most Python builtin functions
