# Multilingual Dictionary in the Semantic Web

Электронное представление Греко-Славяно-Латинского словаря Епифания Славинецкого в формате TEI XML, а также трансформация в RDF.

Словарь на портале Lexonomy: https://www.lexonomy.eu/gsldict


## TEI-encoded-Dictionary ##

[XML файл](https://github.com/wildmary/TEI-encoded-Dictionary/blob/main/dictionary_TEI.xml) с размеченным словарем

[Код](https://github.com/wildmary/TEI-encoded-Dictionary/blob/main/словарь.ipynb) для преобразования .csv таблицы в XML

[Текст](https://github.com/wildmary/TEI-encoded-Dictionary/blob/main/Левченко%20Мария%2C%20курсовая%20работа%20по%20словарю%20Епифания%20Славинецкого.docx) курсовой работы

[Схема](https://github.com/wildmary/TEI-encoded-Dictionary/blob/main/schema.png) структуры XML Файла

[RDF-репрезентация](https://raw.githubusercontent.com/wildmary/TEI-RDF-encoded-Dictionary/main/rdf_entry_representation.png) двух словарных вхождений словаря

[Презентация](https://github.com/wildmary/TEI-encoded-Dictionary/blob/main/Электронное%20представление.pptx) для защиты курсовой

### python package ###

[Ссылка на Pypi](https://pypi.org/project/xmlexicon/)

Установка через командную строку:
```
pip install xmlexicon
```

Импорт библиотеки:
```python
from xmlexicon import xmlexicon
```

Для **конвертации** .csv файла нужно выполнить следующие команды:
```python
epifanii = xmlexicon.Epifanii_dict("whole_dictionary.csv")
epifanii.encode()
epifanii.write_to_xml()
```
Результат будет записан в файл "whole_dictionary_TEI.xml".




Библиотека позволяет также посмотреть **визуализированную статистику** по среднему число русских аналогов на греческую лемму и по количеству вхождений по частям речи:
```python
viz =xmlexicon.Epifanii_visual("whole_dictionary.csv")
viz.analyze()
viz.visualize()
```
Фигура с графиками сохранится в файл "Epifanii_visual.png".



## RDF-encoded-Dictionary ##

[RDF-схема](https://raw.githubusercontent.com/wildmary/TEI-RDF-encoded-Dictionary/main/RDF-schema.png) описания словаря.

[RDF-репрезентация](https://raw.githubusercontent.com/wildmary/TEI-RDF-encoded-Dictionary/main/rdf_entry_representation.png) двух словарных вхождений словаря.

[Упрощенная RDF-репрезентация](https://raw.githubusercontent.com/wildmary/TEI-RDF-encoded-Dictionary/main/Knapiusz.png) связи трех лемм Польско-латинско-греческого тезауруса Григория Кнапского и слов из ГСЛ Епифания Славинецкого.

[Описание](https://github.com/wildmary/TEI-RDF-encoded-Dictionary/blob/main/rdf_entry_Turtle.ttl) словарных вхождений βαλίος  и βαλιός  в формате Turtle.
