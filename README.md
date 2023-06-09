# Исследование стабильности обучения нейронных сетей на примере размера пакета
  Нейронные сети обучаются с использованием градиентного спуска, при котором оценка ошибки, используемая для обновления весов, рассчитывается на основе подмножества обучающего набора данных. Количество примеров из набора обучающих данных, используемых для оценки градиента ошибки, называется размером пакета и является важным гиперпараметром, влияющим на динамику алгоритма обучения.

  Размер пакета (The batch size) – это гиперпараметр, определяющий количество выборок, которые необходимо обработать перед обновлением внутренних параметров модели. В конце пакета прогнозы сравниваются с ожидаемыми выходными переменными и вычисляется ошибка. Из-за этой ошибки алгоритм обновления используется для улучшения модели, например. двигаться вниз по градиенту ошибки. Набор обучающих данных можно разделить на один или несколько пакетов.

  Когда все обучающие выборки используются для создания одной партии, алгоритм обучения называется пакетным градиентным спуском (batch gradient descent). Когда партия имеет размер одной выборки, алгоритм обучения называется стохастическим градиентным спуском (stochastic gradient descent). Когда размер пакета больше одной выборки и меньше размера обучающего набора данных, алгоритм обучения называется мини-пакетным градиентным спуском (mini-batch gradient descent).

  Результаты исследования: 
  - Batch gradient descent: loss: 0.4542; accuracy: 0.8140; val_loss: 0.4465; val_accuracy: 0.8340. Время обучения: 10.6 сек
  - Stochastic gradient descent: loss: 0.4044; accuracy: 0.8300; val_loss: 0.4574; val_accuracy: 0.8240. Время обучения:  302.92 сек
  - Mini-batch gradient descent: loss: 0.3937; accuracy: 0.8220; val_loss: 0.4350; val_accuracy: 0.8180. Время обучения: 22.43 сек
