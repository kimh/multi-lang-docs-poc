# Design Decisions

## Option 1: subdirectory approach

Create language subdirectories under _cci2/. e.g _cci2/ja/

_cci2/
  welcome.md # English
  ja/
    welcome.md # Japanese

Pros:
  - simple

Cons:
  * Language part in url needs to come after 2.0.
    e.g /2.0/ja/welcome

    But probably we may want url to look like this.
    e.g. /ja/2.0/welcome

## Option 2: collection per language

We can create a different collection for each language in _config.yml

```
collections:
  cci2:
    output: true
    permalink: /2.0/:path/

  cci2_ja:
    output: true
    permalink: /ja/2.0/:path/
```

Pros:
  - We can set lang fragment as the root of the url

  e.g. /ja/2.0/welcome
