# Perceptron-and-Boolean-Functions-AND-OR-NAND-and-XOR.
**The Perceptron is a linear machine learning algorithm for binary classification tasks.**

**It is  the simplest type of neural network model.**

(Perceptron — это линейный алгоритм машинного обучения для задач бинарной классификации.

Это самый простой тип модели нейронной сети.)

**It consists of a single node or neuron that takes a row of data as input and predicts a class label. This is achieved by calculating the weighted sum of the inputs and a bias (set to 1). The weighted sum of the input of the model is called the activation.**

- **Activation** = Weights * Inputs + Bias

**If the activation is above 0.0, the model will output 1.0; otherwise, it will output 0.0**.

- **Predict 1**: If Activation > 0.0
- **Predict 0**: If Activation <= 0.0

(Он состоит из одного узла или нейрона, который принимает строку данных в качестве входных данных и предсказывает метку класса. Это достигается путем вычисления взвешенной суммы входных данных и смещения (установленного на 1). Взвешенная сумма входных данных модели называется активацией.

- **Активация**
    
    = веса * входы + смещение
    

Если активация выше 0,0, модель выдаст 1,0; в противном случае будет выведено 0.0.

- **Прогноз 1**
    
    : если активация> 0,0
    
- **Прогноз 0**
    
    : если активация <= 0,0)
    
    **The Perceptron is a linear classification algorithm. This means that it learns a decision boundary that separates two classes using a line (called a hyperplane) in the feature space. As such, it is appropriate for those problems where the classes can be separated well by a line or linear model, referred to as linearly separable.**
    
    (Персептрон — это алгоритм линейной классификации. Это означает, что он изучает границу решения, которая разделяет два класса с помощью линии (называемой гиперплоскостью) в пространстве признаков. Таким образом, он подходит для тех задач, где классы могут быть хорошо разделены линейной или линейной моделью, называемой линейно разделимой.)
    
    **AND, OR, NAND and XOR.**
    
    **Logic gates are the most basic materials to implement digital components. The use of logic gates ranges from computer architecture to the field of electronics.**
    
    **These gates deal with binary values, either 0 or 1. Different types of gates take different numbers of input, but all of them provide a single output. These logic gates when combined form complicated circuits.**
    

(Логические вентили — это самые основные материалы для реализации цифровых компонентов. Использование логических вентилей варьируется от компьютерной архитектуры до области электроники.

Эти вентили имеют дело с двоичными значениями, либо 0, либо 1. Различные типы вентилей принимают разное количество входных данных, но все они обеспечивают один выход. Эти логические элементы в сочетании образуют сложные схемы.)

**Task:** 

**Create and train a Single-layer Perceptron and MLP (Multi-layered perceptron) , implement an algorithm**

 **for classifying logical functions - AND, OR, NAND and XOR.**

(Задача: Создать и обучить Однослойный Персептрон и MLP ( Multi-layered perceptron) , реализовать алгоритм классификации логических функций -  AND, OR, NAND и XOR.)


## The Perceptron Class

## Structure and Properties

### Input Nodes

**These nodes contain the input to the network. (Эти узлы содержат вход в сеть)**

### Weights and Biases

**These parameters are what we update when we talk about “training” a model. They are initialized to some random value or set to 0 and updated as the training progresses. The bias is analogous to a weight independent of any input node. Basically, it makes the model more flexible, since you can “move” the activation function around.**

(Именно эти параметры мы обновляем, когда говорим об «обучении» модели. Они инициализируются некоторым случайным значением или устанавливаются в 0 и обновляются по мере прохождения обучения. Смещение аналогично весу, независимому от любого входного узла. По сути, это делает модель более гибкой, поскольку вы можете «перемещать» функцию активации.)

### Activation Function

**Though there are many kinds of activation functions, we’ll be using a simple linear activation function for our perceptron. The linear activation function has no effect on its input and outputs it as is.**

(Хотя существует много видов функций активации, мы будем использовать для нашего персептрона простую линейную функцию активации. Линейная функция активации не влияет на входные данные и выводит их как есть.)

### Classification

**We’ll be modelling this as a classification problem, so Class 1 would represent an value of 1, while Class 0 would represent a value of 0.**

(Мы будем моделировать это как проблему классификации, поэтому класс 1 будет представлять значение , равное 1, а класс 0 будет представлять значение 0.)

### Training algorithm

**Here, we cycle through the data indefinitely, keeping track of how many consecutive datapoints we correctly classified. If we manage to classify everything in one stretch, we terminate our algorithm. If not, we reset our counter, update our weights and continue the algorithm.**

(Здесь мы бесконечно циклически перебираем данные, отслеживая, сколько последовательных точек данных мы правильно классифицировали. Если нам удастся классифицировать все за один раз, мы завершаем наш алгоритм. Если нет, мы сбрасываем наш счетчик, обновляем наши веса и продолжаем алгоритм.)


# Analyzing the Results AND, OR, and NAND.

The single-layer perceptron correctly classified the entire data set for the logical functions: AND, OR, and NAND.

Since these functions are linearly separable

( Однослойный персептрон правильно классифицировал весь набор данных для логических функций: AND, OR  и  NAND.

т. к. эти функции линейно разделимы.)

# Analyzing the Results (XOR)

**A single layer perceptron is not enough to model the 2d XOR function, so the learning cycle never ends. this function is not linearly separable. But the XOR function can be modeled by combining AND, OR and NAND single layer perceptrons**

(Однослойного персептрона недостаточно для моделирования функции 2d XOR, поэтому  цикл обучения никогда не заканчивается, т.к. эта функция линейно не разделима. Но функцию XOR можно моделировать путем объединения однослойных персептронов AND, OR и NAND.)

# Modeling the XOR function by combining single-layered perceptrons

( Моделирование функции XOR путем объединения однослойных персептронов)

**The XOR function is basically a combination of an AND, OR and NAND. gate.** 

**(**Функция XOR в основном представляет собой комбинацию AND, OR и NAND.

**XOR(x1, x2) = AND(OR(x1, x2), NAND(x1, x2))**

## This model correctly classified the entire data set for the logical function: XOR.

(Такая модель правильно классифицировала весь набор данных для логическoй функции: XOR.)


# MLP ( Multi-layered perceptron)

**A multi-layered perceptron can have hidden layers. (Многослойный персептрон может иметь скрытые слои.)**

**There are no fixed rules on the number of hidden layers or the number of nodes in each layer of a network. The best performing models are obtained through trial and error.**

(Не существует фиксированных правил по количеству скрытых слоев или количеству узлов в каждом слое сети. Лучшие модели получаются методом проб и ошибок.)

**Let’s go with a single hidden layer with two nodes in it. We’ll be using the sigmoid function in each of our hidden layer nodes and of course, our output node.**

(Давайте возьмем один скрытый слой с двумя узлами в нем. Мы будем использовать сигмовидную функцию в каждом из наших узлов скрытого слоя и, конечно же, в нашем выходном узле.)

## The MLP Class

**This class houses each component of our MLP, from training and the forward pass, to classifying and plotting the decision boundary.**

(Этот класс содержит каждый компонент нашего MLP, от обучения и прямого прохода до классификации и построения границы решения.)

**MLP ( Multi-layered perceptron) correctly classified the entire data set for the logical function: XOR.**

( MLP ( Multi-layered perceptron) правильно классифицировал весь набор данных для логическoй функции: XOR.)
