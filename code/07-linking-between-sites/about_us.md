# Modifying the exmaples
# Playing with intersphinx Intersphinx Examples


## Setting up external targets in `conf.py`

Set up the InterSphinx targets in `conf.py` like this

```
intersphinx_mapping = {
    "sphinx": ("https://www.sphinx-doc.org/en/master/", None),
    "scikit": ("https://scikit-image.org/docs/stable/", None),
    'numpy': ('http://docs.scipy.org/doc/numpy/', None),
    'outerspacem': ('https://mattausc.embl-community.io/outer-spacem/', None),
}
```


## Verifying the URL
To check whether this is the correct URL, you can try to append `objects.inv` to the
URL. If you can download the the objects inventory file this way, the URL is probably correct.

Example:
```bash
wget http://docs.scipy.org/doc/numpy/objects.inv
```

## Link to the external sites

Here are some examples for linking to External sites using Markdown Syntax.
Note that by leaving the `[]` empty, the link title will be taken from the 
title of the role or page that is linked to. 

```
Let's talk about the power of [](sphinx:ref-role).

Here, we link to [](scikit:license)

Let's try numpy [](numpy:license)

Outerspacem [](outerspacem:usage)

Outerspacem [](outerspacem:installation)
```

This results in the following output:

Let's talk about the power of [](sphinx:ref-role).

Here, we link to [](scikit:license)

Let's try numpy [](numpy:license)

Outerspacem [](outerspacem:usage)

Outerspacem [](outerspacem:installation)

