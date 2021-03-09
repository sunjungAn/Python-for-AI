**명령행 파싱 모듈**

**아무것도 하지 않는 코드**
```
import argparse
parser = argpase.ArgumentParser()
parser.parse_args()
```


**위치 인자**
```
import argparse
parser = argpase.ArgumentParser()
parser.add_argument("echo")
parser.parse_args()
print(args.echo)
```
> + add_argument() : 프로그램이 받고 싶은 명령행 옵션을 지정하기 위해 사용
> + parse_args() : 실제로 지정된 옵션으로부터 온 데이터를 돌려줌


```
import argparse
parser = argpase.ArgumentParser()
parser.add_argument("square", help = "display a square of a given number", type = int)
#argument를 문자열로 취급하여 str 과 int끼리의 연산이 불가능! --> argument를 int로 취급하도록 설정 
parser.parse_args()
print(args.square**2)
```


