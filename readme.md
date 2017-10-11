

```python
    %reload_ext literacy
```


```python
about.md
```


about.md


---

# Developer

All build logic is contained with in the `readme.ipynb` file.  Use `nbconvert` to execute this notebook with the command below.

    !jupyter nbconvert --to markdown --config config.py readme.ipynb
    
## [Conference Website](https://tonyfast.github.io/callistory/)


This project maintains an index of notebooks on the `master` branch.  The Github Pages deployment separates out the HTML and Markdown content from the source documents.   

### [Travis Pages Deployment](https://docs.travis-ci.com/user/deployment/pages/)


```python
    %%file config.py
    c.Exporter.preprocessors.append('literacy.template.Execute')
    c.TemplateExporter.exclude_input=True
    c.TemplateExporter.exclude_input_prompt=True
```


    %%file config.py
    c.Exporter.preprocessors.append('literacy.template.Execute')
    c.TemplateExporter.exclude_input=True
    c.TemplateExporter.exclude_input_prompt=True


    Overwriting config.py



```python
    !jupyter nbconvert --to markdown *.ipynb
    !jupyter nbconvert --config config.py index.ipynb 
```


    !jupyter nbconvert --to markdown *.ipynb
    !jupyter nbconvert --config config.py index.ipynb 


    [NbConvertApp] Converting notebook about.ipynb to markdown
    [NbConvertApp] Writing 790 bytes to about.md
    [NbConvertApp] Converting notebook contributing.ipynb to markdown
    [NbConvertApp] Writing 857 bytes to contributing.md
    [NbConvertApp] Converting notebook index.ipynb to markdown
    [NbConvertApp] Writing 422 bytes to index.md
    [NbConvertApp] Converting notebook long.ipynb to markdown
    [NbConvertApp] Writing 1140 bytes to long.md
    [NbConvertApp] Converting notebook participants.ipynb to markdown
    [NbConvertApp] Writing 30 bytes to participants.md
    [NbConvertApp] Converting notebook readme.ipynb to markdown
    [NbConvertApp] Writing 3197 bytes to readme.md
    [NbConvertApp] Converting notebook short.ipynb to markdown
    [NbConvertApp] Writing 120 bytes to short.md
    [NbConvertApp] Converting notebook index.ipynb to html
    [NbConvertApp] Executing notebook with kernel: python3
    [NbConvertApp] Writing 258634 bytes to index.html



```python
contributing.md
```



# [contributing](contributing.ipynb)

`callistory` treats DIY event organization as open source piece of software.

## [Submit questions and suggestions through the github issues](https://github.com/tonyfast/callistory/issues)

We hope that community participation can assist future organizers in producing diy technology events.

## Development

* __[readme.ipynb](readme.ipynb)__ provides instruction for external services.
* __[about.ipynb](about.ipynb)__ provides information about the event.  Who what where when how why.
* __[long.ipynb](long.ipynb)__ provides provides long format presentations information.
* __[short.ipynb](short.ipynb)__ provides provides short format presentations information.
* __[participants.ipynb](participants.ipynb)__ provides extra information about the conference participants.

# [Code of Conduct](code_of_conduct.md)




```python
    %%file custom.css
    .output code {display: none;}
```


    %%file custom.css
    .output code {display: none;}


    Writing custom.css

