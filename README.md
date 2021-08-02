# Сжатие изображений

_Идея проекта_: создание нейронной сети, которая могла бы преобразовывать картинку в тензор меньшего размера, а потом этот тензор превращать в исходную картинку.

_Способы применения:_
 - Для передачи видео более эффективно(Разбиваем видео на кадры, к каждому кадру применяем нейронную сеть (encoder) - получаем тензор. Передаём этот тензор. Принимающая сторона разворачивает тензор в картинку с помощью decoder. Собираем видео.)
 - Для уменьшения памяти, необходимой для хранения фото и видео

Для обучения использовался датасет https://www.kaggle.com/andrewmvd/animal-faces.

_Архитектура нейронной сети - encoder-decoder_

Предварительно картинки преобразовываются к размеру 512*512. 

![](https://github.com/AnastasiaCHAS/Image-compression/blob/main/ar.png)
![](https://github.com/AnastasiaCHAS/Image-compression/blob/main/la.png)

_Результат_ - сжатие в 8 раз!

_Примеры работы_

Слева - исходная картинка

Справа - картинка, которая сжимается, а потом разжимается с помощью нейронной сети.

![](https://github.com/AnastasiaCHAS/Image-compression/blob/main/1.jpg)
![](https://github.com/AnastasiaCHAS/Image-compression/blob/main/2.jpg)

_Точность равна 99%._

(Точность - среднее значение MSE по всем пикселям.)
