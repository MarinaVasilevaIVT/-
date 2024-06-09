Результат:
[Репозиторий](https://github.com/MarinaVasilevaIVT/Lab.Work8) \
[Сайт](https://marinavasilevaivt.github.io/Lab.Work8/)


На основе материалов темы реализовать развертывание проекта на Sphinx и продемонстрировать это развертывание и его результат в отчете. Выполнить установку и развертывание проекта с использованием виртуального окружения и использовать poetry.
1. Для начала устанавливаем Sphinx.
```
pip install Sphinx
```
2. Создаем виртуальное оружение
```
python -m venv myenv
```
3. Активация виртуального окружения в Windows
```
.\myenv\Scripts\activate
```
4. Инициализация проекта
```
# Создание директории для проекта
mkdir my_sphinx_project
cd my_sphinx_project

# Инициализация проекта Sphinx
sphinx-quickstart
```
5. Далее для создания именно документации по моему проекту необходимо:
* перенести main.py в ту же директорию
* создать файл main.rst с содержанием
```
.. _main:

Main Module
===========
.. automodule:: main
   :members:
   :undoc-members:
   :show-inheritance:
```
* в index.rst добавить:
```
.. toctree::
 :maxdepth: 2
 :caption: Contents:

 main
```
* в conf.py добавить:
```
import os
import sys
sys.path.insert(0, os.path.abspath('.'))
```
```
extensions = ['sphinx.ext.autodoc']
```
* и запустить собираться файл с помощью команды:
```
.\make.bat html
```
