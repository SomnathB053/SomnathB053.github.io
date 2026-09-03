
```
bundle exec jekyll serve -H 0.0.0.0 -w --config _config.yml,_config_docker.yml
```


# 3 types of content
- Projects
- Publications
- Logs


# Info

```YAML

    ---
    title: "WIP Project"
    published: false
    ---
```
Any file with published: false in its front matter will remain hidden in production builds while keeping your files cleanly organized in the actual collection folders where they belong.



