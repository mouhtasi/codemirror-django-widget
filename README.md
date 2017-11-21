settings.py:
```python
INSTALLED_APPS = (
    ...
    'codemirror',
    ...
)

# Default config
CODEMIRROR_CONFIG = {
    'lineNumbers': True,
}
```

Usage:
forms.py in the main app:
```python
from django import forms
from codemirror.widgets import CodeMirror

class SomeForm(forms.Form):
    text = forms.CharField(widget=CodeMirror(mode='python'))
```

