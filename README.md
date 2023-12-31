# NumPy 배열 슬라이싱

파이썬에서, 특히 NumPy 배열에서 제공하는 중요한 기능 중 하나는 배열 슬라이싱입니다.  
아래는 해당 문법에 대한 설명입니다.

## `;`를 사용한 배열 슬라이싱

`;`는 배열에서 특정 축을 따라 모든 요소를 선택하는 데 사용됩니다.  
2차원 배열에서는 `;`가 행과 열을 나누는 데 사용됩니다.  
다음은 예시입니다:

```python
import numpy as np

x = np.array([[0, 1, 2, 3],
              [4, 5, 6, 7],
              [8, 9, 10, 11]])

# 두 번째 열의 모든 요소 선택
selected_column = x[:, 1]
print(selected_column)
```
#[::.]를 사용한 배열 슬라이싱
[::.]는 배열 슬라이싱에서 특정 간격으로 요소를 선택하는 데 사용됩니다.  
일반적인 구문은 [시작:끝:간격]입니다.  
다음은 예시입니다:

```python
# 행과 열을 따라 슬라이싱에 ; 사용
rows_and_cols = x[1:3, ::2]
print(rows_and_cols)
```
이 예제에서 x[1:3, ::2]는 인덱스가 1과 2인 행을 선택하고 간격이 2인 열을 선택하여 특정 부분을 추출합니다.
이러한 배열 슬라이싱 기능을 활용하면 NumPy 배열에서 특정 부분을 효과적으로 선택할 수 있습니다.

# NumPy에서 차원 추가하기
`np.newaxis`를 사용한 슬라이싱은 차원을 추가하는 특별한 용도로 사용됩니다.  
이를 통해 배열 `x`의 차원을 하나 늘릴 수 있습니다.  
구체적으로는 첫 번째 차원에 새로운 축을 추가합니다.  
예를 들어, 2차원 배열 `x`가 다음과 같다고 가정합시다:

```python
import numpy as np

x = np.array([[0, 1, 2],
              [3, 4, 5],
              [6, 7, 8]])
```
x[np.newaxis, :, :]는 x 배열에 새로운 차원을 추가합니다.  
결과적으로 3차원 배열이 됩니다.  
새로 추가된 차원은 크기가 1인 차원입니다.  
따라서 결과는 다음과 같습니다:

```python
array([[[0, 1, 2],
        [3, 4, 5],
        [6, 7, 8]]])
```
이러한 방식으로 차원을 추가하면, 데이터를 새로운 차원에 재구성할 수 있으며, 이는 특정 NumPy 함수 또는 연산에 필요한 배열의 형태를 맞추는 데 유용할 수 있습니다.
