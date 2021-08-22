## BEHAVIOR_BASED_DETECTION

### Injector
- Ư�� ���μ����� dll�� Injection, Ejection �����ִ� ����

```
Injection.exe -i <process ��> <dll ��>
```

### detector
- Hooking �� API�� ���� �߻��ϴ� debug log�� �޾Ƽ�, Ư�� ���μ����� �ó������� �����ϴ��� ���Ͽ�, �Ǽ� Ű�ΰŶ�� �ǴܵǸ� �˸��� ���� ���� ���θ� ����ڿ��� �˷��ִ� ���α׷�

### globalhook
- global hooking�� �����ϴ� dll
- CreateProcessA,� CreateProcessW�� ��ŷ�Ͽ�, �ڽ� ���μ����� globalhook.dll �� myhook.dll �� �ڵ����� Injection�� �����ֵ��� �Ѵ�.

### myhook
- ������� Ž���� �ʿ��� API�� ��ŷ�ϴ� dll

### Implementation of Scenario Algorithm
- �Ǽ��ڵ� �ó������� ������ �� ���

## Requirements
- Windows7 32bit
- Visual studio 2019

## ����
- Clone from Github
```
git clone https://github.com/NPclown/BOB10_Behavior_Based_Detection.git
cd BOB10_Behavior_Based_Detection
cd src

Build.sln ����
```

- Build ����
```
x86���� ���带 ����
```

- dll ���� �̵�
```
BOB10_Behavior_Based_Detection\Build\Debugx86
BOB10_Behavior_Based_Detection\Build\Releasex86 

������ �����Ǵ� globalhook.dll �� myhook.dll�� C:\Windows\System32 �� �̵�
```

- Detector ����

- Injector ����
```
# �������� ������ ��
Injector.exe -i explorer.exe globalhook.dll

# �������� ������ ��
Injector.exe -e explorer.exe globalhook.dll
```



