## 2018 Part 1
### [Lesson 1](http://course.fast.ai/lessons/lesson1.html)
#### Аренда мощностей с GPU

|Сервис|Цена с CPU/час|Цена с GPU/час|примечания|
|---|---|---|---|
|crestle.com|0.059|0.59|Есть Jupiter|
|paperspace.com|   |0.4-0.9|Есть разные конфиги, получаешь машину целиком, 5$+ - storage|
|AWS|   |   |   |
|AWS spot instance|   |   |   |
|GCP|   |   |   |

Копирование конфига от Джереми и настройка машины в соответствии с ним:
`curl http://files.fast.ai/setup/paperspace | bash`
После выполнения ребутнуться надо.
Команды для запуска ноутбука:
```
cd fastai
git pull
conda env update
jupiter notebook
```

#### Консольные команды из Jupiter
`!ls {PATH}`
Команды после `!` выполнятся в консоли, а не в блокноте
Содержимое фигурных скобок - переменная питона.

#### Структура папок и файлов проекта image classification на Keras
```cats_dogs/
../train/
../train/cats/
../train/cats/cat_class_sample_001.jpg
../train/cats/cat_class_sample_002.jpg
......................................
../train/cats/cat_class_sample_NNN.jpg
../train/dogs/
../train/dogs/dog_class_sample_001.jpg
../train/dogs/dog_class_sample_002.jpg
......................................
../train/dogs/dog_class_sample_NNN.jpg
../valid/
../valid/cats/
../valid/cats/cat_class_valid_sample_001.jpg
../valid/cats/cat_class_valid_sample_002.jpg
......................................
../valid/cats/cat_class_valid_sample_NNN.jpg
../valid/dogs/
../valid/dogs/dog_class_valid_sample_001.jpg
../valid/dogs/dog_class_valid_sample_002.jpg
......................................
../valid/dogs/dog_class_valid_sample_NNN.jpg
```
