```python
import numpy as np
```

# 넘파이

넘파이는 1차원 배열 뿐만 아니라 다차원 배열도 작성 가능합니다.


```python
A = np.array([[1,2],[3,4]])
print(A)
```


```python
A.shape
```




    (2, 2)



다음과 같이 형태가 같은 행렬끼리의 산술 연산도 가능합니다.


```python
B = np.array([[3,0],[0,6]])
A+B
```




    array([[ 4,  2],
           [ 3, 10]])




```python
A * B
```




    array([[ 3,  0],
           [ 0, 24]])



# 브로드캐스트

넘파이에선 형상이 다른 배열끼리도 계산 가능합니다.


```python
A = np.array([[1,2],[3,4]])
B = np.array([10,20])
A*B
```




    array([[10, 40],
           [30, 80]])



# 원소 접근


```python
X = np.array([[51,55],[14,19],[0,4]])
print(X)
```

    [[51 55]
     [14 19]
     [ 0  4]]
    


```python
X[0]
```




    array([51, 55])




```python
X[0][1]
```




    55




```python
X=X.flatten()
print(X)
```

    [51 55 14 19  0  4]
    


```python
X[np.array([0,2,4])]
```




    array([51, 14,  0])



배열 X 에서 15보다 큰 값의 참 여부


```python
X>15
```




    array([ True,  True, False,  True, False, False])



배열 X안에서 15보다 큰값들 추출


```python
X[X>15]
```




    array([51, 55, 19])




```python

```
