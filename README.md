# LangChain Blog Generator 🤖

This Python script uses the Streamlit library to create a web application that generates blogs using the LangChain library.

## Script Overview

The script starts by importing the necessary libraries:

```python
import streamlit as st
from langchain.prompts import PromptTemplate
from langchain.llms import CTransformers
```

Then, it defines a function ```getLLamaresponse``` that generates a blog given an input text, the number of words, and the blog style:

```python
def getLLamaresponse(input_text, no_words, blog_style):
    ...
