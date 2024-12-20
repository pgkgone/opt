В данном задании было необходимо конвертировать обученную нейронную сеть в формат ONNX, после чего сравнить скорость работы pytorch модели с ONNX runtime.\

Обучение моделей и сравнение результатов проводилось на cifar-10 датасете.

```
Evaluation of the best PyTorch model:
Accuracy of the best model on the 10000 test images: 72.63%
Evaluation time: 17.58 seconds

Accuracy per class for the best model on the test set:
Accuracy for class: plane is 85.8 %
Accuracy for class: car   is 94.2 %
Accuracy for class: bird  is 60.0 %
Accuracy for class: cat   is 56.9 %
Accuracy for class: deer  is 57.4 %
Accuracy for class: dog   is 62.7 %
Accuracy for class: frog  is 84.2 %
Accuracy for class: horse is 76.3 %
Accuracy for class: ship  is 84.9 %
Accuracy for class: truck is 63.9 %
```

```
Evaluation of the ONNX model on the test images:
Accuracy of the ONNX model on the 10000 test images: 72.22%
Evaluation time: 15.59 seconds

Accuracy per class for the ONNX model on the test set:
Accuracy for class: plane is 82.0 %
Accuracy for class: car   is 84.3 %
Accuracy for class: bird  is 59.1 %
Accuracy for class: cat   is 49.1 %
Accuracy for class: deer  is 67.0 %
Accuracy for class: dog   is 69.7 %
Accuracy for class: frog  is 83.2 %
Accuracy for class: horse is 68.2 %
Accuracy for class: ship  is 78.6 %
Accuracy for class: truck is 81.0 %
```

По результатам выполнения видно, что скорость работы увеличилась ~12% (15.59/17.58). Точность незначительно упала ~0.005% (72.22/72.63).\
Таким образом, преобразование в ONNX и использование ONNX runtime является хорошим способом увеличить производительность модели.
