

# HStream

Easiest interactive python web app using htmx and semantic html

# Usage

`pip install hstream`

```
# main.py

from hstream import hs

hs.text_input('What's your name?', default_value = 'friend')
hs.markdown(f"Welcome {visitor_name}")
```

`python -m hstream main.py`

![hstream demo](docs/hello_hstream.png)

# Motivation

Love Streamlit but:

- find it hard to deploy
- impossible to customise beyond PoC phase
- overly complicated

H-(html)-Stream stream is built with semantic html, FastApi and htmx to provide a fast and simple framework for rapid web app developmenet that follows traditional frontend/server architecture (or atleast follow it closer than Streamlit).

# Features

- [x] only reloads changed components after the visitor provides input
- [x] live server reload on file change (through univorn)
- [x] semantic html and basic html manipulation from within script
- [x] basic components - see below
- [x] swap stylesheet
- [ ] auto ssl certs for easy deployment
- [ ] complex html manipulation from within script (setting attributes)

## Components

`hs.teax_input`

`hs.checkbox`

`hs.slider`: numeric slider input

`hs.plot`: output matplotlib figures to the user

`hs.image`: display an image

`hs.html`: allows more complex formatting, for example 

`hs.stylesheet_href = https://unpkg.com/@vladocar/basic.css@1.0.3/css/basic.css` to use a diffrent classless css framework

```
with hs.html('form'):
    hs.text_input('Name'):
    hs.checkbox('Would you like to be my firend?')
```

# Technologies

Big thanks to the following libraries in particular

- Streamlit
- htmx
- Yattag
- MVP.css
- FastAPI
- uvicorn