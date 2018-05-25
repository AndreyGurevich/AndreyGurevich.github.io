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

#### Нейронные сети
##### Несколько слоёв:
* Input layer
* Hidden layers
* Output layer

##### Теорема Цыбенко, Универсальная теорема аппроксимации
теорема, доказанная Джорджем Цыбенко в 1989 году, которая утверждает, что искусственная нейронная сеть прямой связи (англ. feed-forward; в которых связи не образуют циклов) с одним скрытым слоем может аппроксимировать любую непрерывную функцию многих переменных с любой точностью. Условиями являются: достаточное количество нейронов скрытого слоя, удачный подбор {\displaystyle \mathbf {w} _{1},\mathbf {w} _{2},\dots ,\mathbf {w} _{N},\mathbf {\alpha } ,} {\displaystyle \mathbf {w} _{1},\mathbf {w} _{2},\dots ,\mathbf {w} _{N},\mathbf {\alpha } ,} и {\displaystyle \mathbf {\theta } } {\displaystyle \mathbf {\theta } }, где

{\displaystyle \mathbf {w} _{i}} {\displaystyle \mathbf {w} _{i}} — веса между входными нейронами и нейронами скрытого слоя
{\displaystyle \mathbf {\alpha } } {\displaystyle \mathbf {\alpha } } — веса между связями от нейронов скрытого слоя и выходным нейроном
{\displaystyle \mathbf {\theta } } {\displaystyle \mathbf {\theta } } — коэффициент «предвзятости» для нейронов скрытого слоя.

#### Градиентный спуск

#### CNN (Convolutional Neural Network)
Convolution (Свёртка) - метод обработки даннах. Например, массив 3*3 (9 пикселов картинки) превращается в одно число, умножая каждое из 9 чисел на коэффициент и суммирую результат.

**relu** - отрицательные числа заменяет нулём, положительные оставляет как есть.




 
