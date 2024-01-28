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

This function uses the ```CTransformers``` class from the ```langchain.llms``` module to generate the blog.

Next, the script sets the page configuration using Streamlit's ```set_page_config``` function:

```python
st.set_page_config(page_title="LangChain", 
                   page_icon="🤖", 
                   layout="centered", 
                   initial_sidebar_state="collapsed")
```
The script then creates the Streamlit application interface, which includes a header, text input fields for the blog topic and number of words, a select box for the blog style, and a button to generate the blog:
```python
st.header("Generate Blogs 🤖")
...
submit=st.button("Generate Blog")
```
Finally, when the "Generate Blog" button is clicked, the script calls the ```getLLamaresponse``` function and writes the generated blog to the Streamlit application:
```python
if submit:
    st.write(getLLamaresponse(input_text, no_words, blog_style))
```
