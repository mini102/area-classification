# area-classification
cs231n's tutorial 

## reference
> cs231n neural network training tutorial (hard cording)
> https://cs231n.github.io/neural-networks-case-study/

## library
![image](https://user-images.githubusercontent.com/73246476/153516270-11ea86f8-f6f3-433b-a436-908d93bb0342.png)
![image](https://user-images.githubusercontent.com/73246476/153516273-c89798ad-54ef-4bc7-ba19-96349155ea69.png)
![image](https://user-images.githubusercontent.com/73246476/153516277-cf5fb167-09aa-47e7-af04-47defb76f671.png)

## Training data / testing data
- dots that randomly made and have a class (label)
![image](https://user-images.githubusercontent.com/73246476/153516389-8874ca2b-4796-4c6b-be47-7f75a0c38e57.png)

## result
![image](https://user-images.githubusercontent.com/73246476/153516649-8dd96041-88af-428c-9170-f4b3b5d21e95.png)
> visualize model's prediction at background for dots using matplot

## Algorithm
클래스가 다른 점들(색이 다른 점들)을 랜덤으로 생성하고 점들을 x, 점들이 속한 각각의 클래스(color)를 y라고 둔다.

**“X를 보고 각 점들이 속한 클래스를 예측하는 것이 목표”**

![image](https://user-images.githubusercontent.com/73246476/153516993-a3dffa92-daec-4ab3-9e5a-df468da5be52.png)
> initialization을 마친 W와 b를 연산한 값에 ReLU를 적용하여 non linear하게 hidden layer를 만들어준다.

![image](https://user-images.githubusercontent.com/73246476/153517012-cacb5ab6-30e3-4e67-856b-f331415282b5.png)
> hidden layer에 initialization을 마친 W2와 b2를 연산한 값을 score(각 클래스에 대한 예측 점수)로 둔다.

이 score에 softmax를 적용한 다음, y값 (정답)과의 loss를 구하고, backpropagation 과정을 통해 loss의 gradient를 구한다.
gradient에 따라 W,b,W2,b2를 계속 업데이트 해주면서 loss가 최소인, 즉 최적의 가중치와 bias를 찾아가는 알고리즘.

