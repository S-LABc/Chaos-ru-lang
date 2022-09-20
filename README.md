# Chaos-ru-lang
#### Визуализации, соединяющие теорию хаоса, фракталы и логистическое отображение!
###### Автор [Jonny Hyman](https://www.jonnyhyman.com), 2020
Этот репозиторий является копией с целью перевода. В исходниках скриптов есть небольшие изменения.
- Оригинальный [репозиторий](https://github.com/jonnyhyman/Chaos)
- Оригинальное [readme](https://github.com/jonnyhyman/Chaos/blob/master/README.md)
- Видео от [Veritasium](https://www.youtube.com/watch?v=ovJcsL7vyrk)
- Видео в русской озвучке от [Vert Dider](https://www.youtube.com/watch?v=DH1cv0Rdf2w&ab_channel=VertDider)

Это не библиотека, а набор независимых скриптов на [Python](https://www.python.org/)! Таким образом, в скриптах есть небольшое повторение кода.

# Быстрый старт для новичков
Инструкцию, предлагаемую автором проекта, можно прочитать в оригинальном [readme](https://github.com/S-LABc/Chaos-ru-lang/blob/main/README_ORIG.md). Я использовал немного другой способ.
- Тестирование проводилось на Python 3.7.9 под ОС Windows 10
- Для редактирования скриптов можно использовать [Notepad++](https://notepad-plus-plus.org/downloads/)
#### Установить
Эти три модуля являются основными и используются во всех скриптах. Обратите внимание, что версии **вообще всех** модулей и Python **ВАЖНЫ**!
- [Python 3.7.9 Windows](https://www.python.org/downloads/release/python-379/)
- Модуль математических вычислений [Numpy](https://numpy.org) : 
    ```
    pip install numpy==1.18.1
    ```
- Модуль ускорения вычислений [Numba](https://numba.pydata.org) :
    ```
    pip install numba==0.48.0
    ```

#### Порядок запуска скриптов (Windows 10)
0. Скачать репозиторий zip архивом и разархивировать 
1. Открыть разархивированную папку с файлами скриптов
2. В строке адреса ввести "cmd" и нажать Enter
3. Ввести команду запуска нужного скрипта, например `python logistic_interactive.py`, или только его название `logistic_interactive.py`
4. Если после установки Python выбрали галочку добавления пути в систему, то можно запускать скрипты двойным кликом ЛКМ

#### Если у вас проблемы с запуском
0. Погуглить проблему
1. Если вам кажется, что проблема в **исходном коде**, напишите сообщение в разделе [Issues](https://github.com/jonnyhyman/Chaos/issues) оригинального репозитория

----

## Логистическое отображение
Эта визуализация создает график попуяций, график функции и график бифуркаций для визуализации логистического отображения.
- Шрифт "Avenir Next" лицензирован для macOS. Другие ОС подтянут свой доступный шрифт.
```
python logistic_interactive.py
```
![Interactive](https://github.com/S-LABc/Chaos-ru-lang/blob/main/images/logistic-interactive-ru.png?raw=true)
#### Дополнительные пакеты
- Модуль графического фреймворка [PyQt5](https://pypi.org/project/PyQt5/) :
    ```
    pip install pyqt5==5.14.1
    ```
- Модуль научно-исследовательских графиков [PyQtGraph](https://www.pyqtgraph.org/) :
    ```
    pip install pyqtgraph==0.10.0
    ```
#### Горячие клавиши:
- Пробел: проиграть/пауза
- Backspace: сбросить отображение и анимацию
----

## Множество Мандельброта с логистическим отображением
Здесь мы видим набор Мандельброта на плоскости xy и итерации набора Мандельброта на оси z. Это создает график бифуркации под множеством Мандельброта!
- Окончательная визуализация достигается за счет рендеринга 1000x1000x1000 вокселей с передискретизацией в 16 раз.
- Настраиваемые параметры находятся после комметария *# ---- PARAMETERS*.
```
python logistic_mandelbrot.py
```
![Mandelbrot Set within Logistic Map GIF](https://github.com/S-LABc/Chaos-ru-lang/blob/main/images/logistic-mandelbrot.gif?raw=true)
#### Дополнительные пакеты
- Модуль визуализации 2D/3D на основе OpenGL [Vispy](http://vispy.org) :
    ```
    pip install vispy==0.6.4
    ```
- Модуль для визуализаций [Matplotlib](https://matplotlib.org) :
    ```
    pip install matplotlib==3.1.2
    ```
- Модуль доступа к фунциям OpenGL [PyOpenGL](https://pypi.org/project/PyOpenGL/) :
    ```
    pip install pyopengl==3.1.5
    ```
- [ffmpeg](https://www.ffmpeg.org) если вы хотите соединять отрендеренные кадры в контейнер .movs (сделать видео файл😅)
    - Windows: [Установить chocolatey](https://chocolatey.org) потом
    ```
    choco install ffmpeg
    ```
----

## Логистическое отображение с приближением
```
python logistic_zoom.py
```
![Logistic Map Zoom GIF](https://github.com/S-LABc/Chaos-ru-lang/blob/main/images/logistic-zoom.gif?raw=true)
#### Дополнительные пакеты
- Модуль для визуализаций 2D/3D на основе OpenGL [Vispy](http://vispy.org) :
    ```
    pip install vispy==0.6.4
    ```
  - Примечание: Для финальной версии визуализации использовалась пользовательская версия Vispy, модифицированная для улучшения внешнего вида осей. Эта версия Vispy опубликована автором [здесь](https://github.com/jonnyhyman/vispy).
#### Горячие клавиши:
- Пробел: запуск/пауза симуляции
- Точка: симуляция следующей итерации (вперед)
- Запятая: симуляция предыдущей итерации (назад)

## Создание исполняемого файла
Будет работать только со скриптом "Логистическое отображение". Исполняемый файл для ОС Windows есть в [релизах](https://github.com/S-LABc/Chaos-ru-lang/releases), работает без Python
#### Установить
- Модуль [PyInstaller](https://pypi.org/project/pyinstaller/) :
```
pip install PyInstaller==5.4.1
```
#### Запустить
Ключ **-F** соберет все в один исполяемый файл и разместит его в папке **dist** рядом со скриптом
```
pyinstaller -F logistic_mandelbrot.py
```
