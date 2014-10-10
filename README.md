pythonjs
========

This is a *very basic* Python->JavaScript translator written in Python. This translator will convert relatively simple Python/NumPy functions to JavaScript, using our [numpy.js](https://github.com/vispy/numpy.js). Typically, these functions will be interactivity functions (like callback functions reacting to mouse movements, key strokes...) and emitting GLIR (OpenGL) commands to update the visualization.

We'll start from PythonJS and Pythonium code. We'll only support the most common Python/NumPy syntactic constructs.
