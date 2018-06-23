# flask-desktop
flask-desktop is a Python module that allows you to convert Flask apps into cross platform desktop apps with three lines of code.

This repo is a fork of the original, located [here](https://github.com/Widdershin/flask-desktophttps://github.com/Widdershin/flask-desktop). 
I wished to use it for a personal project, but it was using a slightly older version of Flask than I wanted, so I forked it, and updated the requirements.

# Installation:
I'll put this up on pip at some point but for now: 

`pip install git+git://github.com/cornjuliox/flask-desktop.git`

# Usage:
```python
    from webui import WebUI # Add WebUI to your imports
    from flask import Flask, render_template, request
    
    app = Flask(__name__)
    ui = WebUI(app, debug=True) # Create a WebUI instance

    @app.route('/')
    def hello_world():
        return 'This should display in a browser-like window.'

    if __name__ == '__main__':
      ui.run() #replace app.run() with ui.run(), and that's it
```

flask-desktop is powered by PyQt5, and should run on Windows, Mac and Linux. You can even create standalone executables using PyInstaller!

# License
flask-desktop is licensed under the MIT License. See the LICENSE file for more details.
