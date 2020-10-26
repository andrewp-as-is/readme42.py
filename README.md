<!--
https://readme42.com
-->



[![](https://img.shields.io/badge/OS-Unix-blue.svg?longCache=True)]()
[![](https://img.shields.io/pypi/v/readme42.svg?maxAge=3600)](https://pypi.org/project/readme42/)
[![](https://img.shields.io/npm/v/readme42.svg?maxAge=3600)](https://www.npmjs.com/package/readme42)[![](https://img.shields.io/badge/License-Unlicense-blue.svg?longCache=True)](https://unlicense.org/)
[![](https://github.com/andrewp-as-is/readme42.py/workflows/tests42/badge.svg)](https://github.com/andrewp-as-is/readme42.py/actions)

### Installation
```bash
$ [sudo] pip install readme42
```

```bash
$ [sudo] npm i -g readme42
```

#### Examples
https://readme42.com/templates/username/template
```html
{% if examples %}
### Examples
{{ examples }}
{% endif %}

{% if links %}
### Links
{{ links }}
{% endif %}
```

cli
```bash
$ export README42_TOKEN="XXX" # https://readme42.com/token/
$ export README42_TEMPLATE="username/template"
$ readme42 . > README42.md
```

python api:
```python
url = 'https://api.readme42.com/templates'
headers = {'Authorization': 'Token README42_TOKEN'}

data = dict(
    examples=open('examples.md').read(),
    links=open('links.md').read()
)
r = requests.post(url,headers=headers,data=data)

open('README.md','w').write(r.text)
```

#### Links
+   [readme42.com](https://readme42.com/)

<p align="center">
    <a href="https://readme42.com/">readme42.com</a>
</p>
