#  Третье задание #
### У нас есть некоторый датакласс: ###

```Python
from dataclasses import dataclass

@dataclass
class Task:
    name: str
    siblings: bool = None
    mother: str = None
    father: str = None
    siblings_by_mother: list[str, ...] | str = None
    owner: str = None
    owner_species: str = None
    species_occupation: str = None
    occupation_class: str = None
    occupation_subclass: str = None
```

### Нужно наполнить датакласс данными из JSON-файла, который лежит в этом репозитории. ###
**Ещё важное уточнение:**  
_Давай сделаем вид, что тут не 4 объекта в "task", а несколько десятков тысяч.  
То есть нужен алгоритм, который считает данные и наполнит ими датакласс вне зависимости от того, сколько в JSON'е лежит данных._