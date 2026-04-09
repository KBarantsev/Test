[![Typing SVG](https://readme-typing-svg.herokuapp.com?color=%2336BCF7&lines=Human+face+detector)](https://git.io/typing-svg)

## Аннотация
Проект посвящен обучению нескольких сверточных нейросетей детектировать лица людей на фотографиях. Были взяты три модели из фреймворка torchvision.models.detection: FasterRCNN, SSD и RetinaNet. 
Обучение проводилось на датасете WIDER FACE http://shuoyang1213.me/WIDERFACE/ (в тренировочной выборке 12876 фото, валидационной 3222 фото). 
Backbone модели выбран обученным на Image Net. Головы, отвечающие за регрессию и классификацию, выбраны необученными.  Несколько последних слоев backbone, регрессор и классификатор были оставлены обучаемыми, остальные слои были заморожены.
При обучении контролировались метрики Precision, Recall, F1 и для итоговой оценки качества модели Average precision. Использование RetinaNet c двумя тренируемыми слоями backbone показало наилучший результат Average precision=0.7393.
