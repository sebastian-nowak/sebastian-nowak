
### Hey there! 👋

```python

from dataclasses import dataclass
from typing import Tuple


class Meta(type):
    def __new__(cls, name, bases, attrs):
        new_cls = super().__new__(cls, name, bases, attrs)
        return dataclass(unsafe_hash=True, frozen=True)(new_cls)

class Bio(metaclass=Meta):
    name        : str = 'Sebastian Daniel Nowak'
    designation : str = 'Software Engineer'
    base        : str = 'Warsaw, Poland'
    hobbies     : str = 'Road cycling, climbing, photography'

class Stack(metaclass=Meta):
    languages   : Tuple[str, ...] = ('JavaScript', 'Python', 'Java', 'C++')
    databases   : Tuple[str, ...] = ('MySQL', 'PostgreSQL', 'MongoDB', 'Redis')
    frameworks  : Tuple[str, ...] = ('React', 'Vue.js')
    misc        : Tuple[str, ...] = ('Bazel', 'Docker')
```


### Get in touch

<a href="https://sdnowak.com"><img width="22px" valign="top" src="https://raw.githubusercontent.com/edent/SuperTinyIcons/9f13284dfaa5ec877e42fff53f0bc6ba6ff82953/images/svg/dev_to.svg"/></a>&nbsp; Home: https://sdnowak.com

<a href="https://linkedin.com/in/sebastian-daniel-nowak/"><img width="22px" valign="top" src="https://raw.githubusercontent.com/edent/SuperTinyIcons/099dc12b59179d07d534069bc8551718f786d91a/images/svg/linkedin.svg"/></a>&nbsp; LinkedIn: https://linkedin.com/in/sebastian-daniel-nowak/

<a href="https://instagram.com/sd.nowak/"><img width="22px" valign="top" src="https://raw.githubusercontent.com/edent/SuperTinyIcons/099dc12b59179d07d534069bc8551718f786d91a/images/svg/instagram.svg"/></a>&nbsp; Instagram: https://instagram.com/sd.nowak/
