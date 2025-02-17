## Container > Kubernetes > 사용 가이드

## 클러스터
클러스터는 사용자의 Kubernetes를 구성하는 인스턴스들의 그룹입니다.

### 클러스터 생성
Kubernetes 서비스를 사용하려면 먼저 클러스터를 생성해야 합니다. **Container > Kubernetes** 서비스 페이지에서 **클러스터 생성** 버튼을 클릭하면 클러스터 생성 페이지가 나타납니다. 클러스터 생성에 필요한 항목은 다음과 같습니다.

| 항목 | 설명 |
| --- | --- |
| 클러스터 이름 | Kubernetes 클러스터의 이름, 20자 이내로 영문 소문자와 숫자, '-'만 입력 가능하며 영문 소문자로 시작해야 하고 영문 소문자 또는 숫자로 끝나야 합니다. |
| Kubernetes 버전 | 사용할 Kubernetes 버전 |
| VPC | 클러스터에 연결할 VPC 네트워크 |
| 서브넷 | VPC에 정의된 서브넷 중 클러스터를 구성하는 인스턴스에 연결할 서브넷 |
| 이미지 | 클러스터를 구성하는 인스턴스에 사용할 이미지 |
| 가용성 영역 | 기본 노드 그룹 인스턴스를 생성할 영역 |
| 인스턴스 타입 | 기본 노드 그룹 인스턴스 사양 |
| 노드 수 | 기본 노드 그룹 인스턴스 수 |
| 키 페어 | 기본 노드 그룹 접근에 사용할 키 페어 |
| 블록 스토리지 타입 | 기본 노드 그룹 인스턴스의 블록 스토리지 종류 |
| 블록 스토리지 크기 | 기본 노드 그룹 인스턴스의 블록 스토리지 크기 |

필요한 정보를 입력하고 **클러스터 생성** 버튼을 클릭하면 클러스터 생성이 시작됩니다. 클러스터 목록에서 상태를 확인할 수 있습니다. 생성하는 데는 약 10분 정도 걸립니다. 클러스터 설정에 따라 더 오래 걸릴 수도 있습니다.


### 클러스터 조회
생성한 클러스터는 **Container > Kubernetes** 서비스 페이지에서 확인할 수 있습니다. 클러스터를 선택하면 하단에 클러스터 정보가 나타납니다.

| 항목 | 설명 |
| --- | --- |
| 클러스터 이름 | Kubernetes 클러스터의 이름과 ID |
| 노드 수 | 클러스터를 구성하는 모든 노드 인스턴스 수 |
| Kubernetes 버전 | 사용 중인 Kubernetes 버전 |
| VPC | 클러스터에 연결된 VPC 네트워크 |
| 서브넷 | 클러스터를 구성하는 노드 인스턴스에 연결된 서브넷 |
| API 엔드포인트 | 클러스터에 접근해 조작하기 위한 API 엔드포인트 URI |
| 설정 파일 | 클러스터에 접근해 조작하기 위해 필요한 설정 파일 다운로드 버튼 |

### 클러스터 삭제
삭제할 클러스터를 선택하고 **클러스터 삭제** 버튼을 클릭하면 삭제가 진행됩니다. 삭제하는 데는 약 5분 정도 걸립니다. 클러스터의 상태에 따라 더 오래 걸릴 수도 있습니다.

## 노드 그룹
노드 그룹은 Kubernetes를 구성하는 워커 노드 인스턴스들의 그룹입니다.

### 노드 그룹 조회
클러스터 목록에서 클러스터 이름을 클릭하면 노드 그룹 목록을 확인할 수 있습니다. 노드 그룹을 선택하면 하단에 노드 그룹 정보가 나타납니다.

* 기본 정보
**기본 정보** 탭에서는 다음과 정보를 확인할 수 있습니다.

| 항목 | 설명 |
| --- | --- |
| 노드 그룹 이름 | 노드 그룹 이름과 ID |
| 클러스터 이름 | 노드 그룹이 속한 클러스터의 이름과 ID |
| Kubernetes 버전 | 사용 중인 Kubernetes 버전 |
| 가용성 영역 | 노드 그룹 인스턴스가 생성된 영역 |
| 인스턴스 타입 | 노드 그룹 인스턴스 사양 |
| 이미지 타입 | 노드 그룹 인스턴스에 사용한 이미지 종류 |
| 블록 스토리지 크기 | 노드 그룹 인스턴스의 블록 스토리지 크기 |
| 생성일 | 노드 그룹이 생성된 시각 |
| 수정일 | 노드 그룹이 마지막으로 수정된 시각 |

* 노드 목록
**노드 목록** 탭에서는 노드 그룹을 구성하는 인스턴스의 목록을 확인할 수 있습니다.

### 노드 그룹 생성
클러스터를 생성하면 기본 노드 그룹이 생성되지만, 필요에 따라 추가 노드 그룹을 만들 수 있습니다. 기본 노드 그룹의 인스턴스보다 높은 사양의 컨테이너 구동 환경이 필요하거나, 스케일 아웃(scale out, 확장)을 위해 더 많은 워커 노드 인스턴스가 필요한 경우 추가 노드 그룹을 생성해 사용할 수 있습니다. 노드 그룹 목록 페이지에서 **노드 그룹 생성** 버튼을 클릭하면 노드 그룹 생성 페이지가 나타납니다. 노드 그룹 생성에 필요한 항목은 다음과 같습니다.

| 항목 | 설명 |
| --- | --- |
| 가용성 영역 | 클러스터를 구성하는 인스턴스를 생성할 영역 |
| 노드 그룹 이름 | 추가 노드 그룹 이름, 20자 이내로 영문 소문자와 숫자, '-'만 입력 가능하며 영문 소문자로 시작해야 하고 영문 소문자 또는 숫자로 끝나야 합니다. |
| 인스턴스 타입 | 추가 노드 그룹 인스턴스 사양 |
| 노드 수 | 추가 노드 그룹 인스턴스 수 |
| 키 페어 | 추가 노드 그룹 접근에 사용할 키 페어 |
| 블록 스토리지 타입 | 추가 노드 그룹 인스턴스의 블록 스토리지 종류 |
| 블록 스토리지 크기 | 추가 노드 그룹 인스턴스의 블록 스토리지 크기 |

필요한 정보를 입력하고 **노드 그룹 생성** 버튼을 클릭하면 노드 그룹 생성이 시작됩니다. 노드 그룹 목록에서 상태를 확인할 수 있습니다. 노드 그룹 생성하는 데는 약 5분 정도 걸립니다. 노드 그룹 설정에 따라 더 오래 걸릴 수도 있습니다.

### 노드 그룹 삭제
노드 그룹 목록에서 삭제하려는 노드 그룹을 선택하고 **노드 그룹 삭제** 버튼을 클릭하면 삭제가 진행됩니다. 노드 그룹 삭제하는 데는 약 5분 정도 걸립니다. 노드 그룹의 상태에 따라 더 오래 걸릴 수도 있습니다.

### 노드 그룹에 노드 추가
동작 중인 노드 그룹에 노드를 추가할 수 있습니다. 노드 그룹 정보 조회 페이지의 노드 목록 탭을 클릭하면 현재 노드 목록이 나타납니다. 노드 추가 버튼을 클릭하고 노드 수를 입력하면 노드가 추가됩니다.

>[주의]
>오토 스케일러가 활성화된 노드 그룹은 수동으로 노드를 추가할 수 없습니다.

### 노드 그룹에서 노드 삭제
동작 중인 노드 그룹에서 노드를 삭제할 수 있습니다. 노드 그룹 정보 조회 페이지의 노드 목록 탭을 클릭하면 현재 노드 목록이 나타납니다. 노드 목록 중 삭제할 노드를 선택하고 노드 삭제 버튼을 클릭하면 확인 대화 상자가 나타납니다. 삭제할 노드 이름을 다시 한번 확인하고 확인 버튼을 클릭하면 노드가 삭제됩니다.

>[주의]
>삭제되는 노드에서 동작하고 있던 파드는 강제 종료 됩니다. 삭제될 노드에서 동작 중인 파드를 안전하게 다른 노드로 옮기기 위해서는 drain 명령을 내려야 합니다. 노드가 drain 된 후에도 새로운 파드는 이 노드에 스케줄링 될 수 있습니다. 새로운 파드가 삭제될 노드에 스케줄링되는 것을 방지하기 위해서는 cordon 명령을 내려야 합니다. 안전한 노드 관리에 대한 좀 더 자세한 내용은 아래 문서를 참고하세요.

>[주의]
>오토 스케일러가 활성화된 노드 그룹은 수동으로 노드를 삭제할 수 없습니다.

* [안전한 노드 drain](https://kubernetes.io/docs/tasks/administer-cluster/safely-drain-node/)
* [수동 노드 관리](https://kubernetes.io/docs/concepts/architecture/nodes/#manual-node-administration)

### GPU 노드 그룹 사용 
Kubernetes를 통한 GPU 기반 워크로드 실행이 필요한 경우, GPU 인스턴스로 구성된 노드 그룹을 생성할 수 있습니다.
클러스터 혹은 노드 그룹 생성 과정에서 인스턴스 타입 선택 시, `g2` 타입을 선택하면 GPU 노드 그룹을 만들 수 있습니다.

> [참고]
> NHN Cloud GPU 인스턴스에서 제공되는 GPU는 NVIDIA 계열입니다. ([사용 가능한 GPU 제원 확인하기](/Compute/GPU%20Instance/ko/overview/#gpu))
> NVIDIA GPU 이용을 위해 Kubernetes에 필요한 nvidia-device-plugin은 GPU 노드 그룹 생성 시 자동으로 설치됩니다.

생성된 GPU 노드에 대한 기본적인 설정 상태 확인 및 간단한 동작 테스트는 다음과 같은 방법을 이용하면 됩니다.

#### 노드 수준의 상태 확인
GPU 노드에 접속한 후, `nvidia-smi` 명령을 실행합니다.
다음과 같은 내용이 출력되면 GPU driver가 정상적으로 동작하는 것입니다.

```
$ nvidia-smi
Mon Jul 27 14:38:07 2020
+-----------------------------------------------------------------------------+
| NVIDIA-SMI 418.152.00   Driver Version: 418.152.00   CUDA Version: 10.1     |
|-------------------------------+----------------------+----------------------+
| GPU  Name        Persistence-M| Bus-Id        Disp.A | Volatile Uncorr. ECC |
| Fan  Temp  Perf  Pwr:Usage/Cap|         Memory-Usage | GPU-Util  Compute M. |
|===============================+======================+======================|
|   0  Tesla T4            Off  | 00000000:00:05.0 Off |                    0 |
| N/A   30C    P8     9W /  70W |      0MiB / 15079MiB |      0%      Default |
+-------------------------------+----------------------+----------------------+

+-----------------------------------------------------------------------------+
| Processes:                                                       GPU Memory |
|  GPU       PID   Type   Process name                             Usage      |
|=============================================================================|
|  No running processes found                                                 |
+-----------------------------------------------------------------------------+ 
```

#### Kubernetes 수준의 상태 확인
`kubectl` 명령을 사용해 클러스터 수준에서 사용 가능한 GPU 리소스 정보를 확인합니다.
아래는 각 노드에서 사용 가능한 GPU 코어의 개수를 출력하도록 하는 명령 및 수행 결과입니다.

```
$ kubectl get nodes -A -o custom-columns='NAME:.metadata.name,GPU Allocatable:.status.allocatable.nvidia\.com/gpu,GPU Capacity:.status.capacity.nvidia\.com/gpu'
NAME                                       GPU Allocatable   GPU Capacity
my-cluster-default-w-vdqxpwisjjsk-node-1   1                 1
```

#### GPU 테스트를 위한 샘플 워크로드 실행
Kubernetes 클러스터에 속한 GPU 노드들은 CPU와 메모리 이외에 `nvidia.com/gpu`와 같은 이름의 리소스를 제공합니다.
GPU를 사용하고 싶다면 `nvidia.com/gpu` 리소스를 할당받도록 아래의 샘플 파일처럼 입력하면 됩니다.

* resnet.yaml
```
apiVersion: v1
kind: Pod
metadata:
  name: resnet-gpu-pod
spec:
  imagePullSecrets:
    - name: nvcr.dgxkey
  containers:
    - name: resnet
      image: nvcr.io/nvidia/tensorflow:18.07-py3
      command: ["mpiexec"]
      args: ["--allow-run-as-root", "--bind-to", "socket", "-np", "1", "python", "/opt/tensorflow/nvidia-examples/cnn/resnet.py", "--layers=50", "--precision=fp16", "--batch_size=64", "--num_iter=90"]
      resources:
        limits:
          nvidia.com/gpu: 1
``` 

위 파일을 실행하면 다음과 같은 결과를 확인할 수 있습니다.

```
$ kubectl create -f resnet.yaml
pod/resnet-gpu-pod created

$ kubectl get pods resnet-gpu-pod
NAME             READY   STATUS    RESTARTS   AGE
resnet-gpu-pod   0/1     Running   0          17s 

$ kubectl logs resnet-gpu-pod -n default -f
PY 3.5.2 (default, Nov 23 2017, 16:37:01)
[GCC 5.4.0 20160609]
TF 1.8.0
Script arguments:
  --layers 50
  --display_every 10
  --iter_unit epoch
  --batch_size 64
  --num_iter 100
  --precision fp16
Training
WARNING:tensorflow:Using temporary folder as model directory: /tmp/tmpjw90ypze
2020-07-31 00:57:23.020712: I tensorflow/stream_executor/cuda/cuda_gpu_executor.cc:898] successful NUMA node read from SysFS had negative value (-1), but there must be at least one NUMA node, so returning NUMA node zero
2020-07-31 00:57:23.023190: I tensorflow/core/common_runtime/gpu/gpu_device.cc:1356] Found device 0 with properties:
name: Tesla T4 major: 7 minor: 5 memoryClockRate(GHz): 1.59
pciBusID: 0000:00:05.0
totalMemory: 14.73GiB freeMemory: 14.62GiB
2020-07-31 00:57:23.023226: I tensorflow/core/common_runtime/gpu/gpu_device.cc:1435] Adding visible gpu devices: 0
2020-07-31 00:57:23.846680: I tensorflow/core/common_runtime/gpu/gpu_device.cc:923] Device interconnect StreamExecutor with strength 1 edge matrix:
2020-07-31 00:57:23.846743: I tensorflow/core/common_runtime/gpu/gpu_device.cc:929]      0
2020-07-31 00:57:23.846753: I tensorflow/core/common_runtime/gpu/gpu_device.cc:942] 0:   N
2020-07-31 00:57:23.847023: I tensorflow/core/common_runtime/gpu/gpu_device.cc:1053] Created TensorFlow device (/job:localhost/replica:0/task:0/device:GPU:0 with 14151 MB memory) -> physical GPU (device: 0, name: Tesla T4, pci bus id: 0000:00:05.0, compute capability: 7.5)
  Step Epoch Img/sec   Loss  LR
     1   1.0     3.1  7.936  8.907 2.00000
    10  10.0    68.3  1.989  2.961 1.65620
    20  20.0   214.0  0.002  0.978 1.31220
    30  30.0   213.8  0.008  0.979 1.00820
    40  40.0   210.8  0.095  1.063 0.74420
    50  50.0   211.9  0.261  1.231 0.52020
    60  60.0   211.6  0.104  1.078 0.33620
    70  70.0   211.3  0.340  1.317 0.19220
    80  80.0   206.7  0.168  1.148 0.08820
    90  90.0   210.4  0.092  1.073 0.02420
   100 100.0   210.4  0.001  0.982 0.00020
```

> [참고]
> GPU가 필요없는 워크로드가 GPU 노드에 할당되는 것을 막고 싶다면 [Taint 및 Toleration 개요](https://kubernetes.io/docs/concepts/scheduling-eviction/taint-and-toleration/)를 참고하세요.

### 오토 스케일러
오토 스케일러는 노드 그룹의 가용 리소스가 부족해 파드(pod)를 스케줄링할 수 없거나 노드의 사용률이 일정 수준 이하로 유지되는 경우 노드의 수를 자동으로 조정하는 기능입니다. 이 기능은 노드 그룹별로 설정할 수 있고, 서로 독립적으로 동작합니다.  이 기능은 Kubernetes 프로젝트의 공식 지원 기능인 cluster-autoscaler 기능을 기반으로 합니다. 자세한 사항은 [Cluster Autoscaler](https://github.com/kubernetes/autoscaler/tree/master/cluster-autoscaler)를 참고하세요.

> [참고]
> Kubernetes 서비스에 적용된 `cluster-autoscaler`의 버전은 `1.19.0`입니다.

#### 용어 정리
오토 스케일러 기능에서 사용하는 용어와 그 의미는 다음과 같습니다.

| 용어 | 의미 |
| --- | --- |
| 증설 | 노드의 수를 증가시키는 것을 말합니다 |
| 감축 | 노드의 수를 감소시키는 것을 말합니다 |

> [주의]
> 워커 노드가 인터넷 연결이 불가능한 환경에서 동작하고 있다면 오토 스케일러 컨테이너 이미지를 워커 노드에 직접 설치해야 합니다. 이 작업이 필요한 대상은 다음과 같습니다.
> 
> * 판교 리전: 2020년 11월 24일 이전에 생성한 노드 그룹
> * 평촌 리전: 2020년 11월 19일 이전에 생성한 노드 그룹
> 
> 오토 스케일러의 컨테이너 이미지 경로는 다음과 같습니다.
>
> * k8s.gcr.io/autoscaling/cluster-autoscaler:v1.19.0

#### 오토 스케일러 설정
오토 스케일러 기능은 노드 그룹별로 설정하고 동작합니다. 오토 스케일러 기능은 아래 경로로 설정할 수 있습니다.

* 클러스터 생성 시 기본 노드 그룹에 설정
* 노드 그룹 추가 시 추가 노드 그룹에 설정
* 생성되어 있는 노드 그룹에 설정

오토 스케일러 활성화 시 아래의 항목에 대해 설정할 수 있습니다.

| 설정 항목 | 의미 | 유효 범위 | 기본값 | 단위 |
| --- | --- | --- | --- | --- |
| 최소 노드 수 | 감축 가능한 최소 노드 수| 1-10 | 1 | 대|
| 최대 노드 수 | 증설 가능한 최대 노드 수| 1-10 | 10 | 대|
| 감축 | 노드 감축 활성 여부 설정 | 활성/비활성 | 활성 | - |
| 리소스 사용량 임계치 | 감축의 기준인 리소스 사용량 임계 영역의 기준값 | 1-100 | 50 | % |
| 임계 영역 유지 시간| 감축 대상이 될 노드의 임계치 이하의 리소스 사용량 유지 시간| 1-1440 | 10 | 분 |
| 증설 후 지연 시간 | 노드 증설 후 감축 대상 노드로 모니터링하기 시작까지의 지연 시간| 1-1440 | 10 | 분 |

> [주의]
> 오토 스케일러가 활성화된 노드 그룹은 수동으로 노드를 추가하거나 삭제할 수 없습니다.

#### 증설 및 감축 조건
아래의 조건을 모두 만족하면 노드를 증설합니다.

* 파드가 스케줄링될 수 있는 노드가 없음
* 현재 노드 수가 최대 노드 수보다 작음

아래의 조건을 모두 만족하면 노드를 감축합니다.

* 노드의 리소스 사용량이 임계치 이하로 임계 영역 유지 시간 동안 유지
* 현재 노드 수가 최소 노드 수보다 큼

특정 노드에 아래 조건을 만족하는 파드가 하나라도 존재한다면 해당 노드는 노드 감축 후보에서 제외됩니다.

* "PodDisruptionBudget"으로 제약 받는 파드
* "kube-system" 네임스페이스의 파드
* "deployment", "replicaset" 등의 제어 오브젝트에 의해 시작되지 않은 파드
* 로컬 스토리지를 사용하는 파드
* "node selector" 등의 제약으로 인해 다른 노드로 이동이 불가능한 파드

좀 더 자세한 증설 및 감축 조건은 [Cluster Autoscaler FAQ](https://github.com/kubernetes/autoscaler/blob/master/cluster-autoscaler/FAQ.md)를 참고하세요.

#### 동작 예시
오토 스케일러의 동작을 예시를 통해 알아봅니다.

##### 1. 오토 스케일러 활성화

대상 클러스터의 기본 노드 그룹의 오토 스케일러 기능을 활성화 합니다. 이 예시에서는 기본 노드 그룹의 노드 수를 1로 생성하였고, 오토 스케일러 설정 항목은 아래와 같이 설정했습니다.

| 설정 항목 | 설정값 |
| --- | --- |
| 최소 노드 수 | 1 |
| 최대 노드 수 | 5 |
| 감축 | 활성 |
| 리소스 사용량 임계치 | 50 |
| 임계 영역 유지 시간| 3 |
| 증설 후 지연 시간 | 5 |

##### 2. 파드 배포

아래의 매니페스트로 파드를 배포합니다.

> [주의]
> 이 매니페스트처럼 컨테이너의 리소스 요청이 명시되어 있어야 합니다.

```yaml
apiVersion: apps/v1
kind: Deployment
metadata:
  name: nginx-deployment
  labels:
    app: nginx
spec:
  replicas: 15
  selector:
    matchLabels:
      app: nginx
  template:
    metadata:
      labels:
        app: nginx
    spec:
      containers:
      - name: nginx
        image: nginx:1.14.2
        ports:
        - containerPort: 80
        resources:
          requests:
            cpu: "100m"
```

배포 요청한 파드의 CPU 리소스 총합이 노드 한 대의 리소스보다 크기 때문에 아래와 같이 몇몇 파드가 `Pending` 상태로 남게 됩니다. 이 상황에서 노드의 증설이 발생합니다.

```
# kubectl get pods
NAME                               READY   STATUS    RESTARTS   AGE
nginx-deployment-756fd4cdf-5gftm   1/1     Running   0          34s
nginx-deployment-756fd4cdf-64gtv   0/1     Pending   0          34s
nginx-deployment-756fd4cdf-7bsst   0/1     Pending   0          34s
nginx-deployment-756fd4cdf-8892p   1/1     Running   0          34s
nginx-deployment-756fd4cdf-8k4cc   1/1     Running   0          34s
nginx-deployment-756fd4cdf-cprp7   0/1     Pending   0          34s
nginx-deployment-756fd4cdf-cvs97   1/1     Running   0          34s
nginx-deployment-756fd4cdf-h7ftk   1/1     Running   0          34s
nginx-deployment-756fd4cdf-hv2fz   0/1     Pending   0          34s
nginx-deployment-756fd4cdf-j789l   0/1     Pending   0          34s
nginx-deployment-756fd4cdf-jrkfj   0/1     Pending   0          34s
nginx-deployment-756fd4cdf-m887q   0/1     Pending   0          34s
nginx-deployment-756fd4cdf-pvnfc   0/1     Pending   0          34s
nginx-deployment-756fd4cdf-wrj8b   1/1     Running   0          34s
nginx-deployment-756fd4cdf-x7ns5   0/1     Pending   0          34s
```

##### 3. 노드 증설 확인

아래는 증설 전의 노드 목록입니다.

```
# kubectl get nodes
NAME                                            STATUS   ROLES    AGE   VERSION
autoscaler-test-default-w-ohw5ab5wpzug-node-0   Ready    <none>   45m   v1.17.6
```

약5~10분 후 아래와 같이 노드가 증설된 것을 확인할 수 있습니다.

```
# kubectl get nodes
NAME                                            STATUS   ROLES    AGE   VERSION
autoscaler-test-default-w-ohw5ab5wpzug-node-0   Ready    <none>   48m   v1.17.6
autoscaler-test-default-w-ohw5ab5wpzug-node-1   Ready    <none>   77s   v1.17.6
autoscaler-test-default-w-ohw5ab5wpzug-node-2   Ready    <none>   78s   v1.17.6
```

`Pending` 상태였던 파드가 노드 증설 이후 정상 스케줄링된 것을 확인할 수 있습니다.

```
# kubectl get pods -o wide
NAME                               READY   STATUS    RESTARTS   AGE     IP            NODE                                            NOMINATED NODE   READINESS GATES
nginx-deployment-756fd4cdf-5gftm   1/1     Running   0          4m29s   10.100.8.13   autoscaler-test-default-w-ohw5ab5wpzug-node-0   <none>           <none>
nginx-deployment-756fd4cdf-64gtv   1/1     Running   0          4m29s   10.100.22.5   autoscaler-test-default-w-ohw5ab5wpzug-node-1   <none>           <none>
nginx-deployment-756fd4cdf-7bsst   1/1     Running   0          4m29s   10.100.22.4   autoscaler-test-default-w-ohw5ab5wpzug-node-1   <none>           <none>
nginx-deployment-756fd4cdf-8892p   1/1     Running   0          4m29s   10.100.8.10   autoscaler-test-default-w-ohw5ab5wpzug-node-0   <none>           <none>
nginx-deployment-756fd4cdf-8k4cc   1/1     Running   0          4m29s   10.100.8.12   autoscaler-test-default-w-ohw5ab5wpzug-node-0   <none>           <none>
nginx-deployment-756fd4cdf-cprp7   1/1     Running   0          4m29s   10.100.12.7   autoscaler-test-default-w-ohw5ab5wpzug-node-2   <none>           <none>
nginx-deployment-756fd4cdf-cvs97   1/1     Running   0          4m29s   10.100.8.14   autoscaler-test-default-w-ohw5ab5wpzug-node-0   <none>           <none>
nginx-deployment-756fd4cdf-h7ftk   1/1     Running   0          4m29s   10.100.8.11   autoscaler-test-default-w-ohw5ab5wpzug-node-0   <none>           <none>
nginx-deployment-756fd4cdf-hv2fz   1/1     Running   0          4m29s   10.100.12.5   autoscaler-test-default-w-ohw5ab5wpzug-node-2   <none>           <none>
nginx-deployment-756fd4cdf-j789l   1/1     Running   0          4m29s   10.100.22.6   autoscaler-test-default-w-ohw5ab5wpzug-node-1   <none>           <none>
nginx-deployment-756fd4cdf-jrkfj   1/1     Running   0          4m29s   10.100.12.4   autoscaler-test-default-w-ohw5ab5wpzug-node-2   <none>           <none>
nginx-deployment-756fd4cdf-m887q   1/1     Running   0          4m29s   10.100.22.3   autoscaler-test-default-w-ohw5ab5wpzug-node-1   <none>           <none>
nginx-deployment-756fd4cdf-pvnfc   1/1     Running   0          4m29s   10.100.12.6   autoscaler-test-default-w-ohw5ab5wpzug-node-2   <none>           <none>
nginx-deployment-756fd4cdf-wrj8b   1/1     Running   0          4m29s   10.100.8.15   autoscaler-test-default-w-ohw5ab5wpzug-node-0   <none>           <none>
nginx-deployment-756fd4cdf-x7ns5   1/1     Running   0          4m29s   10.100.12.3   autoscaler-test-default-w-ohw5ab5wpzug-node-2   <none>           <none>
```

노드 증설에 대한 이벤트는 아래 명령어로 확인할 수 있습니다.

```
# kubectl get events --field-selector reason="TriggeredScaleUp"
LAST SEEN   TYPE     REASON             OBJECT                                 MESSAGE
4m          Normal   TriggeredScaleUp   pod/nginx-deployment-756fd4cdf-64gtv   pod triggered scale-up: [{default-worker-bf5999ab 1->3 (max: 5)}]
4m          Normal   TriggeredScaleUp   pod/nginx-deployment-756fd4cdf-7bsst   pod triggered scale-up: [{default-worker-bf5999ab 1->3 (max: 5)}]
...
```


##### 4. 파드 삭제 후 노드 감축 확인

배포되어 있는 디플로이먼트(deployment)를 삭제하면 배포되어 있던 파드가 삭제됩니다.

```
# kubectl get pods
NAME                               READY   STATUS        RESTARTS   AGE
nginx-deployment-756fd4cdf-5gftm   0/1     Terminating   0          20m
nginx-deployment-756fd4cdf-64gtv   0/1     Terminating   0          20m
nginx-deployment-756fd4cdf-7bsst   0/1     Terminating   0          20m
nginx-deployment-756fd4cdf-8892p   0/1     Terminating   0          20m
nginx-deployment-756fd4cdf-8k4cc   0/1     Terminating   0          20m
nginx-deployment-756fd4cdf-cprp7   0/1     Terminating   0          20m
nginx-deployment-756fd4cdf-h7ftk   0/1     Terminating   0          20m
nginx-deployment-756fd4cdf-hv2fz   0/1     Terminating   0          20m
nginx-deployment-756fd4cdf-j789l   0/1     Terminating   0          20m
nginx-deployment-756fd4cdf-jrkfj   0/1     Terminating   0          20m
nginx-deployment-756fd4cdf-m887q   0/1     Terminating   0          20m
nginx-deployment-756fd4cdf-pvnfc   0/1     Terminating   0          20m
nginx-deployment-756fd4cdf-wrj8b   0/1     Terminating   0          20m
nginx-deployment-756fd4cdf-x7ns5   0/1     Terminating   0          20m
#
# kubectl get pods
No resources found in default namespace.
#
```

잠시 후 노드 감축이 발생하여 노드 수가 1개로 줄어든 것을 확인할 수 있습니다. 노드 감축에 걸리는 시간은 설정에 따라 달라질 수 있습니다.

```
# kubectl get nodes
NAME                                            STATUS   ROLES    AGE   VERSION
autoscaler-test-default-w-ohw5ab5wpzug-node-0   Ready    <none>   71m   v1.17.6
```

노드 감축에 대한 이벤트는 아래 명령어로 확인할 수 있습니다.

```
# kubectl get events --field-selector reason="ScaleDown"
LAST SEEN   TYPE     REASON      OBJECT                                               MESSAGE
13m         Normal   ScaleDown   node/autoscaler-test-default-w-ohw5ab5wpzug-node-1   node removed by cluster autoscaler
13m         Normal   ScaleDown   node/autoscaler-test-default-w-ohw5ab5wpzug-node-2   node removed by cluster autoscaler
```

노드 그룹별 오토 스케일러의 상태 정보는 `configmap/cluster-autoscaler-status`를 통해 확인할 수 있습니다. 이 컨피그맵(configmap)은 노드 그룹별로 서로 다른 네임스페이스에 생성됩니다. 오토 스케일러가 생성하는 노드 그룹별 네임스페이스의 이름 규칙은 다음과 같습니다.

* 형식: nhn-ng-{노드그룹명}
* {노드그룹명}에는 노드 그룹의 이름이 들어갑니다.
* 기본 노드 그룹의 노드 그룹 이름은 "default-worker" 입니다.

기본 노드 그룹에 대한 오토 스케일러의 상태 정보를 확인하는 방법은 다음과 같습니다. 보다 자세한 정보는 [Cluster Autoscaler FAQ](https://github.com/kubernetes/autoscaler/blob/master/cluster-autoscaler/FAQ.md)를 참고하세요.

```
# kubectl get configmap/cluster-autoscaler-status -n nhn-ng-default-worker -o yaml
apiVersion: v1
data:
  status: |+
    Cluster-autoscaler status at 2020-11-03 12:39:12.190150095 +0000 UTC:
    Cluster-wide:
      Health:      Healthy (ready=1 unready=0 notStarted=0 longNotStarted=0 registered=1 longUnregistered=0)
                   LastProbeTime:      2020-11-03 12:39:12.185954244 +0000 UTC m=+43.664545435
                   LastTransitionTime: 2020-11-03 12:38:41.705407217 +0000 UTC m=+13.183998415
      ScaleUp:     NoActivity (ready=1 registered=1)
                   LastProbeTime:      2020-11-03 12:39:12.185954244 +0000 UTC m=+43.664545435
                   LastTransitionTime: 2020-11-03 12:38:41.705407217 +0000 UTC m=+13.183998415
      ScaleDown:   NoCandidates (candidates=0)
                   LastProbeTime:      2020-11-03 12:39:12.185954244 +0000 UTC m=+43.664545435
                   LastTransitionTime: 2020-11-03 12:38:41.705407217 +0000 UTC m=+13.183998415

    NodeGroups:
      Name:        default-worker-f9a9ee5e
      Health:      Healthy (ready=1 unready=0 notStarted=0 longNotStarted=0 registered=1 longUnregistered=0 cloudProviderTarget=1 (minSize=1, maxSize=5))
                   LastProbeTime:      2020-11-03 12:39:12.185954244 +0000 UTC m=+43.664545435
                   LastTransitionTime: 2020-11-03 12:38:41.705407217 +0000 UTC m=+13.183998415
      ScaleUp:     NoActivity (ready=1 cloudProviderTarget=1)
                   LastProbeTime:      2020-11-03 12:39:12.185954244 +0000 UTC m=+43.664545435
                   LastTransitionTime: 2020-11-03 12:38:41.705407217 +0000 UTC m=+13.183998415
      ScaleDown:   NoCandidates (candidates=0)
                   LastProbeTime:      2020-11-03 12:39:12.185954244 +0000 UTC m=+43.664545435
                   LastTransitionTime: 2020-11-03 12:38:41.705407217 +0000 UTC m=+13.183998415

kind: ConfigMap
metadata:
  annotations:
    cluster-autoscaler.kubernetes.io/last-updated: 2020-11-03 12:39:12.190150095 +0000
      UTC
  creationTimestamp: "2020-11-03T12:38:28Z"
  name: cluster-autoscaler-status
  namespace: nhn-ng-default-worker
  resourceVersion: "1610"
  selfLink: /api/v1/namespaces/nhn-ng-default-worker/configmaps/cluster-autoscaler-status
  uid: e72bd1a2-a56f-41b4-92ee-d11600386558
```

> [참고]
> 상태 정보의 내용 중 `Cluster-wide` 영역의 내용은 `NodeGroups` 영역의 내용과 같습니다.

#### HPA(HorizontalPodAutoscale) 기능과 연동한 동작 예시
HPA(Horizontal Pod Autoscaler) 기능은 CPU 사용량 등의 리소스 사용량을 관찰하여 레플리케이션 컨트롤러(ReplicationController), 디플로이먼트(Deployment), 레플리카셋(ReplicaSet), 스테이트풀셋(StatefulSet)의 파드 개수를 자동으로 스케일합니다. 파드 개수를 조절하다 보면 노드에 가용 리소스가 부족하거나 리소스가 많이 남는 상황이 발생할 수 있습니다. 이때 오토 스케일러 기능과 연동하여 노드의 수를 늘이거나 줄일 수 있습니다. 이 예제에서는 HPA 기능과 오토 스케일러 기능을 연동해 동작하는 것을 보여줍니다. HPA에 대한 자세한 설명은 [Horizontal Pod Autoscaler](https://kubernetes.io/docs/tasks/run-application/horizontal-pod-autoscale/) 문서를 참고하세요. 

##### 1. 오토 스케일러 활성화
위의 예제와 같이 오토 스케일러를 활성화 합니다.

##### 2. HPA 설정
웹 요청을 받으면 일정 시간동안 CPU 부하를 생성하는 컨테이너를 배포합니다. 그리고 서비스를 노출시킵니다. 다음은 `php-apache.yaml` 파일의 내용입니다.

```yaml
apiVersion: apps/v1
kind: Deployment
metadata:
  name: php-apache
spec:
  selector:
    matchLabels:
      run: php-apache
  replicas: 1
  template:
    metadata:
      labels:
        run: php-apache
    spec:
      containers:
      - name: php-apache
        image: k8s.gcr.io/hpa-example
        ports:
        - containerPort: 80
        resources:
          limits:
            cpu: 500m
          requests:
            cpu: 200m
---
apiVersion: v1
kind: Service
metadata:
  name: php-apache
  labels:
    run: php-apache
spec:
  ports:
  - port: 80
  selector:
    run: php-apache
```

```
# kubectl apply -f php-apache.yaml
deployment.apps/php-apache created
service/php-apache created
```

이제 HPA를 설정합니다. 위에서 방금 생성한 php-apache deployment 객체에 대해 최소 파드 수 1, 최대 파드 수 30, 목표 CPU load는 50%로 설정합니다.

```
# kubectl autoscale deployment php-apache --cpu-percent=50 --min=1 --max=30
horizontalpodautoscaler.autoscaling/php-apache autoscaled
```

HPA의 상태를 조회해보면 설정값과 현재 상태를 볼 수 있습니다. 아직 CPU 부하를 일으키는 web request를 보내지 않았기 때문에 CPU load가 0% 입니다.

```
# kubectl get hpa
NAME         REFERENCE               TARGETS   MINPODS   MAXPODS   REPLICAS   AGE
php-apache   Deployment/php-apache   0%/50%    1         30        1          80s
```

##### 3. 부하 인가
이제 새로운 터미널에서 부하를 일으키는 파드를 실행합니다. 이 파드는 무한히 웹 요청을 보내게 됩니다. `Ctrl+C`로 멈출 수 있습니다.

```
# kubectl run -i --tty load-generator --rm --image=busybox --restart=Never -- /bin/sh -c "while sleep 0.01; do wget -q -O- http://php-apache; done"
If you don't see a command prompt, try pressing enter.
OK!OK!OK!OK!OK!OK!OK!
```

`kubectl top nodes` 커맨드를 이용해 노드의 현재 리소스 사용량을 확인할 수 있습니다. 부하를 일으키는 파드 실행 후 시간이 흐르면서 CPU 부하가 커지는 것을 확인할 수 있습니다.

```
# kubectl top nodes
NAME                                            CPU(cores)   CPU%   MEMORY(bytes)   MEMORY%
autoscaler-test-default-w-ohw5ab5wpzug-node-0   66m          6%     1010Mi          58%

(잠시 후)

# kubectl top nodes
NAME                                            CPU(cores)   CPU%   MEMORY(bytes)   MEMORY%
autoscaler-test-default-w-ohw5ab5wpzug-node-0   574m         57%    1013Mi          58%
```

HPA의 상태를 조회해보면 CPU load가 증가했고, 이를 맞추기 위해 REPLICAS(=파드 수)가 수가 늘어난 것을 확인할 수 있습니다.

```
# kubectl get hpa
NAME         REFERENCE               TARGETS    MINPODS   MAXPODS   REPLICAS   AGE
php-apache   Deployment/php-apache   250%/50%   1         30        5          2m44s
```

##### 4. 오토 스케일러 동작 확인
파드를 조회해보면 파드의 수가 늘어나면서 일부 파드는 `node-0`에 스케줄링되어 Running 상태가 됐지만 일부는 Pending 상태인 것을 확인할 수 있습니다

```
# kubectl get pods -o wide
NAME                          READY   STATUS    RESTARTS   AGE     IP            NODE                                            NOMINATED NODE   READINESS GATES
load-generator                1/1     Running   0          2m      10.100.8.39   autoscaler-test-default-w-ohw5ab5wpzug-node-0   <none>           <none>
php-apache-79544c9bd9-6f7nm   0/1     Pending   0          65s     <none>        <none>                                          <none>           <none>
php-apache-79544c9bd9-82xkn   1/1     Running   0          80s     10.100.8.41   autoscaler-test-default-w-ohw5ab5wpzug-node-0   <none>           <none>
php-apache-79544c9bd9-cjj9q   0/1     Pending   0          80s     <none>        <none>                                          <none>           <none>
php-apache-79544c9bd9-k6nnt   1/1     Running   0          4m27s   10.100.8.38   autoscaler-test-default-w-ohw5ab5wpzug-node-0   <none>           <none>
php-apache-79544c9bd9-mplnn   0/1     Pending   0          19s     <none>        <none>                                          <none>           <none>
php-apache-79544c9bd9-t2knw   1/1     Running   0          80s     10.100.8.40   autoscaler-test-default-w-ohw5ab5wpzug-node-0   <none>           <none>
```

파드를 스케줄링하지 못하는 상황이 바로 오토 스케일러의 노드 증설 조건입니다. Cluster Autoscaler 파드가 제공하는 상태 정보를 조회해보면 ScaleUp이 InProgress 상태가 된 것을 확인할 수 있습니다.

```
# kubectl get cm/cluster-autoscaler-status -n nhn-ng-default-worker -o yaml
apiVersion: v1
data:
  status: |+
    Cluster-autoscaler status at 2020-11-24 13:00:40.210137143 +0000 UTC:
    Cluster-wide:
      Health:      Healthy (ready=1 unready=0 notStarted=0 longNotStarted=0 registered=1 longUnregistered=0)
                   LastProbeTime:      2020-11-24 13:00:39.930763305 +0000 UTC m=+1246178.729396969
                   LastTransitionTime: 2020-11-10 02:51:14.353177175 +0000 UTC m=+13.151810823
      ScaleUp:     InProgress (ready=1 registered=1)
                   LastProbeTime:      2020-11-24 13:00:39.930763305 +0000 UTC m=+1246178.729396969
                   LastTransitionTime: 2020-11-24 12:58:34.83642035 +0000 UTC m=+1246053.635054003
      ScaleDown:   NoCandidates (candidates=0)
                   LastProbeTime:      2020-11-24 13:00:39.930763305 +0000 UTC m=+1246178.729396969
                   LastTransitionTime: 2020-11-20 01:42:32.287146552 +0000 UTC m=+859891.085780205

    NodeGroups:
      Name:        default-worker-bf5999ab
      Health:      Healthy (ready=1 unready=0 notStarted=0 longNotStarted=0 registered=1 longUnregistered=0 cloudProviderTarget=2 (minSize=1, maxSize=3))
                   LastProbeTime:      2020-11-24 13:00:39.930763305 +0000 UTC m=+1246178.729396969
                   LastTransitionTime: 2020-11-10 02:51:14.353177175 +0000 UTC m=+13.151810823
      ScaleUp:     InProgress (ready=1 cloudProviderTarget=2)
                   LastProbeTime:      2020-11-24 13:00:39.930763305 +0000 UTC m=+1246178.729396969
                   LastTransitionTime: 2020-11-24 12:58:34.83642035 +0000 UTC m=+1246053.635054003
      ScaleDown:   NoCandidates (candidates=0)
                   LastProbeTime:      2020-11-24 13:00:39.930763305 +0000 UTC m=+1246178.729396969
                   LastTransitionTime: 2020-11-20 01:42:32.287146552 +0000 UTC m=+859891.085780205
...
```

잠시 후 노드(node-8)가 하나 늘어난 것을 확인할 수 있습니다.

```
# kubectl get nodes
NAME                                            STATUS     ROLES    AGE   VERSION
autoscaler-test-default-w-ohw5ab5wpzug-node-0   Ready      <none>   22d   v1.17.6
autoscaler-test-default-w-ohw5ab5wpzug-node-8   Ready      <none>   90s   v1.17.6
```

Pending 상태였던 파드 모두 정상 스케줄링되어 Running 상태가 된 것을 확인할 수 있습니다.

```
# kubectl get pods -o wide
NAME                          READY   STATUS    RESTARTS   AGE     IP            NODE                                            NOMINATED NODE   READINESS GATES
load-generator                1/1     Running   0          5m32s   10.100.8.39   autoscaler-test-default-w-ohw5ab5wpzug-node-0   <none>           <none>
php-apache-79544c9bd9-6f7nm   1/1     Running   0          4m37s   10.100.42.3   autoscaler-test-default-w-ohw5ab5wpzug-node-8   <none>           <none>
php-apache-79544c9bd9-82xkn   1/1     Running   0          4m52s   10.100.8.41   autoscaler-test-default-w-ohw5ab5wpzug-node-0   <none>           <none>
php-apache-79544c9bd9-cjj9q   1/1     Running   0          4m52s   10.100.42.5   autoscaler-test-default-w-ohw5ab5wpzug-node-8   <none>           <none>
php-apache-79544c9bd9-k6nnt   1/1     Running   0          7m59s   10.100.8.38   autoscaler-test-default-w-ohw5ab5wpzug-node-0   <none>           <none>
php-apache-79544c9bd9-mplnn   1/1     Running   0          3m51s   10.100.42.4   autoscaler-test-default-w-ohw5ab5wpzug-node-8   <none>           <none>
php-apache-79544c9bd9-t2knw   1/1     Running   0          4m52s   10.100.8.40   autoscaler-test-default-w-ohw5ab5wpzug-node-0   <none>           <none>
```

부하를 위해 실행해두었던 파드(`load-generator`)를 `Ctrl+C`로 중단시키면 잠시 후 부하가 줄어들게 됩니다. 부하가 줄면 파드가 점유하던 CPU 사용량이 줄어들어 파드의 수가 줄어들게 됩니다.

```
# kubectl get hpa
NAME         REFERENCE               TARGETS   MINPODS   MAXPODS   REPLICAS   AGE
php-apache   Deployment/php-apache   0%/50%    1         30        1          31m
```

파드의 수가 줄어들어 노드의 리소스 사용량이 줄어들면 결국 노드 감축이 발생합니다. 새로 추가되었던 node-8이 감축된 것을 확인할 수 있습니다.

```
# kubectl get nodes
NAME                                            STATUS   ROLES    AGE   VERSION
autoscaler-test-default-w-ohw5ab5wpzug-node-0   Ready    <none>   22d   v1.17.6
```


### 예약 스크립트
클러스터를 생성할 때와 추가 노드 그룹을 생성할 때, 예약 스크립트를 등록할 수 있습니다. 예약 스크립트 기능에는 다음과 같은 특징이 있습니다.

* 기능 설정
    * 이 기능은 워커 노드 그룹별로 설정할 수 있습니다.
    * 클러스터 생성 시 입력한 예약 스크립트는 기본 워커 노드 그룹에 적용됩니다.
    * 추가 노드 그룹 생성 시 입력한 예약 스크립트는 해당 워커 노드 그룹에 적용됩니다.
    * 워커 노드 그룹이 생성된 후에는 예약 스크립트의 내용을 변경할 수 없습니다.
* 스크립트 실행 시점
    * 예약 스크립트는 워커 노드 초기화 과정 중 인스턴스 초기화 과정에서 실행됩니다.
    * 예약 스크립트가 실행된 후, 해당 인스턴스를 '워커 노드 그룹'의 워커 노드로 설정하고 등록합니다.
* 스크립트 내용
    * 예약 스크립트의 첫번째 줄은 반드시 #! 으로 시작해야 합니다.
    * 스크립트 최대 크기는 64KB입니다.
    * 스크립트는 root 권한으로 실행됩니다.
    * 스크립트 실행 기록은 아래 위치에 저장됩니다.
        * 스크립트 종료 코드: `/var/log/userscript.exitcode`
        * 스크립트 표준 출력 및 표준 에러 스트림: `/var/log/userscript.output`


## 클러스터 관리
원격의 호스트에서 클러스터를 조작하고 관리하려면 Kubernetes가 제공하는 명령줄 도구(CLI)인 `kubectl`이 필요합니다.

### kubectl 설치
kubectl은 특별한 설치 과정 없이 실행 파일을 다운로드해 바로 사용할 수 있습니다. 운영체제별 다운로드 경로는 다음과 같습니다.

| 운영체제 | 다운로드 커맨드 |
| --- | --- |
| Linux | curl -LO https://storage.googleapis.com/kubernetes-release/release/v1.15.7/bin/linux/amd64/kubectl |
| MacOS | curl -LO https://storage.googleapis.com/kubernetes-release/release/v1.15.7/bin/darwin/amd64/kubectl |
| Windows | curl -LO https://storage.googleapis.com/kubernetes-release/release/v1.15.7/bin/windows/amd64/kubectl.exe |

그 외 설치 방법과 옵션 등 자세한 사항은 [Install and Set Up kubectl](https://kubernetes.io/docs/tasks/tools/install-kubectl/) 문서를 참고하세요.

#### 권한 변경
다운로드한 파일은 기본적으로 실행 권한이 없습니다. 실행 권한을 추가해야 합니다.

```
$ chmod +x kubectl
```

#### 위치 변경 또는 경로 지정
어느 경로에서든 kubectl을 실행할 수 있도록 환경 변수에 지정된 경로로 옮기거나, kubectl이 있는 경로를 환경 변수에 추가합니다.

* 환경 변수에 지정된 경로로 위치 변경
```
$ sudo mv kubectl /usr/local/bin/
```

* 환경 변수에 경로 추가
```
// kubectl이 있는 경로에서 실행
$ export PATH=$PATH:$(pwd)
```

### 설정
kubectl로 Kubernetes 클러스터에 접근하려면 클러스터 설정 파일(kubeconfig)이 필요합니다. NHN Cloud 웹 콘솔에서 **Container > Kubernetes** 서비스 페이지를 열고 접근할 클러스터를 선택합니다. 하단 **기본 정보** 탭에서 **설정 파일** 항목의 **다운로드** 버튼을 클릭해 설정 파일을 다운로드합니다. 다운로드한 설정 파일은 원하는 위치로 옮겨 kubectl 실행 시 참조할 수 있도록 준비합니다.

> [주의]
> NHN Cloud 웹 콘솔에서 다운로드한 설정 파일은 클러스터 정보와 인증을 위한 토큰 등이 포함되어 있습니다. 설정 파일이 있으면 해당 Kubernetes 클러스터에 접근할 수 있는 권한을 갖게 됩니다. 설정 파일을 절대로 분실하지 않도록 주의하시기 바랍니다.

kubectl은 실행할 때마다 클러스터 설정 파일이 필요합니다. 따라서 매번 `--kubeconfig` 옵션을 이용해 클러스터 설정 파일을 지정해야 합니다. 그러나 환경 변수에 클러스터 설정 파일 경로가 저장되어 있다면 매번 옵션을 지정하지 않아도 됩니다.

```
$ export KUBECONFIG={클러스터 설정 파일 경로}
```

클러스터 설정 파일 경로를 환경 변수에 저장하고 싶지 않다면 kubectl의 기본 설정 파일인 `$HOME/.kube/config`로 복사해 사용할 수도 있습니다. 그러나 클러스터를 여러 개 운영한다면 환경 변숫값을 변경하는 방법이 편리합니다.

### 연결 확인
`kubectl version` 명령어로 정상 설정되었는지 확인합니다. 문제가 없다면 `Server Version`이 출력됩니다.

```
$ kubectl version
Client Version: version.Info{Major:"1", Minor:"15", GitVersion:"v1.15.7", GitCommit:"6c143d35bb11d74970e7bc0b6c45b6bfdffc0bd4", GitTreeState:"clean", BuildDate:"2019-12-11T12:42:56Z", GoVersion:"go1.12.12", Compiler:"gc", Platform:"darwin/amd64"}
Server Version: version.Info{Major:"1", Minor:"15", GitVersion:"v1.15.7", GitCommit:"6c143d35bb11d74970e7bc0b6c45b6bfdffc0bd4", GitTreeState:"clean", BuildDate:"2019-12-11T12:34:17Z", GoVersion:"go1.12.12", Compiler:"gc", Platform:"linux/amd64"}
```

* Client Version: 실행한 kubectl 파일의 버전 정보
* Server Version: 클러스터를 구성하고 있는 Kubernetes 버전 정보

### CSR(CertificateSigningRequest)
Kubernetes의 인증 API(Certificate API)를 통해 Kubernetes API 클라이언트를 위한 X.509 인증서(certificate)를 요청하고 발급할 수 있습니다. CSR 자원은 인증서를 요청하고, 요청에 대해 승인/거부를 결정할 수 있도록 합니다. 자세한 사항은 [Certificate Signing Requests](https://kubernetes.io/docs/reference/access-authn-authz/certificate-signing-requests/) 문서를 참고하세요.

#### CSR 요청과 발급 승인 예제
먼저 개인키(private key)를 생성합니다. 인증서 생성에 관한 자세한 내용은 [Certificates](https://kubernetes.io/docs/concepts/cluster-administration/certificates/) 문서를 참고하세요.

```
# openssl genrsa -out dev-user1.key 2048
Generating RSA private key, 2048 bit long modulus
...........................................................................+++++
..................+++++
e is 65537 (0x010001)

# openssl req -new -key dev-user1.key -subj "/CN=dev-user1" -out dev-user1.csr
```

생성한 개인키 정보를 포함하는 CSR 자원을 생성해 인증서 발급을 요청합니다.

```
# BASE64_CSR=$(cat dev-user1.csr | base64 | tr -d '\n')
# cat <<EOF > csr.yaml -
apiVersion: certificates.k8s.io/v1beta1
kind: CertificateSigningRequest
metadata:
  name: dev-user1
spec:
  groups:
  - system:authenticated
  request: ${BASE64_CSR}
  usages:
  - digital signature
  - key encipherment
  - server auth
  - client auth
EOF

# kubectl apply -f csr.yaml
certificatesigningrequest.certificates.k8s.io/dev-user1 created
```

등록된 CSR은 `Pending` 상태입니다. 이 상태는 발급 승인 또는 거부를 기다리는 상태입니다.

```
# kubectl get csr
NAME        AGE   REQUESTOR          CONDITION
dev-user1   6s    system:unsecured   Pending
```

이 인증서 발급 요청에 대해 승인 처리합니다.

```
# kubectl certificate approve dev-user1
certificatesigningrequest.certificates.k8s.io/dev-user1 approved
```

CSR을 다시 확인해보면 `Approved,Issued` 상태로 변경된 것을 확인할 수 있습니다.
```
# kubectl get csr
NAME        AGE    REQUESTOR          CONDITION
dev-user1   114s   system:unsecured   Approved,Issued
```

인증서는 다음과 같이 조회할 수 있습니다. 인증서는 status의 certificate 필드의 값입니다.

```
# kubectl get csr/dev-user1 -o yaml
apiVersion: certificates.k8s.io/v1beta1
kind: CertificateSigningRequest
metadata:
  annotations:
    kubectl.kubernetes.io/last-applied-configuration: |
      {"apiVersion":"certificates.k8s.io/v1beta1","kind":"CertificateSigningRequest","metadata":{"annotations":{},"name":"dev-user1"},"spec":{"groups":["system:authenticated"],"request":"LS0tLS...(이하 생략)","usages":["digital signature","key encipherment","server auth","client auth"]}}
  creationTimestamp: "2020-12-07T06:32:53Z"
  name: dev-user1
  resourceVersion: "3202"
  selfLink: /apis/certificates.k8s.io/v1beta1/certificatesigningrequests/dev-user1
  uid: b22477eb-0abc-4fc4-8a79-f6516751a940
spec:
  groups:
  - system:masters
  - system:authenticated
  request: LS0tLS...(이하 생략)
  usages:
  - digital signature
  - key encipherment
  - server auth
  - client auth
  username: system:unsecured
status:
  certificate: LS0tLS...(이하 생략)
  conditions:
  - lastUpdateTime: "2020-12-07T06:34:43Z"
    message: This CSR was approved by kubectl certificate approve.
    reason: KubectlApprove
    type: Approved
```

> [주의]
> 이 기능은 클러스터 생성 시점이 아래 기간에 해당하는 경우에만 제공됩니다.
> 
> * 판교 리전: 2020년 12월 29일 이후에 생성한 클러스터
> * 평촌 리전: 2020년 12월 24일 이후에 생성한 클러스터

### 승인 컨트롤러(admission controller) 플러그인
승인 컨트롤러는 Kubernetes API 서버 요청을 가로채 객체를 변경하거나 요청을 거부할 수 있습니다. 승인 컨트롤러에 대한 자세한 설명은 [승인 컨트롤러](https://kubernetes.io/docs/reference/access-authn-authz/admission-controllers/)를 참고하세요. 그리고 승인 컨트롤러의 사용 에제는 [승인 컨트롤러 가이드](https://kubernetes.io/blog/2019/03/21/a-guide-to-kubernetes-admission-controllers/)를 참고하세요.

클러스터 생성 시점에 따라 승인 컨트롤러에 적용되는 플러그인의 종류가 다릅니다. 자세한 내용은 리전별 생성 시점에 따른 플러그인 목록을 참고하세요.

#### 판교 리전 2021년 2월 22일 이전에 생성한 클러스터 및 평촌 리전 2021년 2월 17일 이전에 생성한 클러스터

* DefaultStorageClass
* DefaultTolerationSeconds
* LimitRanger
* MutatingAdmissionWebhook
* NamespaceLifecycle
* NodeRestriction
* PersistentVolumeClaimResize
* Priority
* ResourceQuota
* RuntimeClass
* ServiceAccount
* StorageObjectInUseProtection
* TaintNodesByCondition
* ValidatingAdmissionWebhook

#### 판교 리전 2021년 2월 23일 이후에 생성한 클러스터 및 평촌 리전 2021년 2월 18일 이후에 생성한 클러스터

* DefaultStorageClass
* DefaultTolerationSeconds
* LimitRanger
* MutatingAdmissionWebhook
* NamespaceLifecycle
* NodeRestriction
* PersistentVolumeClaimResize
* PodSecurityPolicy(신규 추가)
* Priority
* ResourceQuota
* RuntimeClass
* ServiceAccount
* StorageObjectInUseProtection
* TaintNodesByCondition
* ValidatingAdmissionWebhook

### 클러스터 업그레이드
NHN Cloud Kubernetes 서비스는 동작 중인 Kubernetes 클러스터의 Kubernetes 구성 요소 업그레이드를 지원합니다. 

#### Kubernetes 버전 차이 지원 정책
Kubernetes 버전은 `x.y.z`로 표현됩니다. `x`는 메이저 버전, `y`는 마이너 버전, `z`는 패치 버전입니다. 기능이 추가되면 메이저 버전 혹은 마이너 버전을 올리고, 버그 수정과 같이 이전 버전과 호환되는 기능을 제공하면 패치 버전을 올립니다. 좀 더 자세한 내용은 [Semantic Versioning 2.0.0](https://semver.org/)을 참고하세요.

Kubernetes 클러스터는 동작 중인 상태에서 Kubernetes 구성 요소를 업그레이드할 수 있습니다. 이를 위해 Kubernetes 구성 요소별로 Kubernetes 버전 차이에 따른 기능 지원 여부를 정의하고 있습니다. 마이너 버전을 기준으로 한 단계의 버전 차이는 상호 기능 호환을 지원함으로써 동작 중인 클러스터의 Kubernetes 구성 요소 업그레이드를 지원합니다. 또 구성 요소 종류 별로 업그레이드 순서를 정의하고 있습니다. 좀 더 자세한 내용은 [Version Skew Policy](https://kubernetes.io/releases/version-skew-policy/)를 참고하세요.

#### 기능 동작 방식
NHN Cloud에서 지원하는 Kubernetes 클러스터 업그레이드 기능의 동작 방식에 대해 설명합니다. 

##### Kubernetes 버전 관리
NHN Cloud의 Kubernetes 클러스터는 클러스터 마스터와 워커 노드 그룹 별로 Kubernetes 버전을 관리합니다. 마스터의 Kubernetes 버전은 클러스터 조회 화면에서 확인할 수 있고, 워커 노드 그룹의 Kubernetes 버전은 각 워커 노드 그룹 조회 화면에서 확인할 수 있습니다. 

##### 업그레이드 규칙
NHN Cloud의 Kubernetes 클러스터 버전 관리 방식과 Kubernetes 버전 차이 지원 정책에 의해 구성 요소별로 순서에 맞게 업그레이드해야 합니다. NHN Cloud의 Kubernetes 클러스터 업그레이드 기능에 적용되는 규칙은 다음과 같습니다.

* 마스터와 각 워커 노드 그룹 별로 업그레이드 명령을 실행해야 합니다. 
* 마스터의 Kubernetes 버전과 모든 워커 노드 그룹의 Kubernetes 버전이 일치해야 업그레이드가 가능합니다.
* 마스터가 가장 먼저 업그레이드 한 후 워커 노드 그룹을 업그레이드할 수 있습니다. 
* 현재 버전의 다음 버전(마이너 버전 기준 +1)으로 업그레이드 가능합니다. 
* 다운그레이드는 지원하지 않습니다. 
* 다른 기능의 동작으로 인해 클러스터가 업데이트 중인 상태에서는 업그레이드가 불가능합니다. 

다음 예시는 Kubernetes 버전을 업그레이드 과정에서 업그레이드 가능 여부를 표로 나타낸 것입니다. 예시에 사용된 조건은 다음과 같습니다. 

* NHN Cloud가 지원하는 Kubernetes 버전 목록: v1.17.6, v1.18.19, v1.19.10
* 클러스터는 v1.17.6으로 생성

| 상태 | 마스터 버전 | 마스터 업그레이드 가능 여부 | 워커 노드 그룹 버전 | 워커 노드 그룹 업그레이드 가능 여부
| --- | :-: | :-: | :-: | :-: |
| 초기 상태| v1.17.6 | 가능① | v1.17.6 | 불가능 ② | 
| 마스터 업그레이드 후 상태 | v1.18.19 | 불가능 ③ | v1.17.6 | 가능 ④ | 
| 워커 노드 그룹 업그레이드 후 상태 | v1.18.19 | 가능 ① | v1.18.19 | 불가능 ② |
| 마스터 업그레이드 후 상태 | v1.19.10 | 불가능 ③ | v1.18.19 | 가능 ④ | 
| 워커 노드 그룹 업그레이드 후 상태 | v1.19.10 | 불가능 ⑤ | v1.19.10 | 불가능 ② |

주석

* ① 마스터와 모든 워커 노드 그룹의 버전이 일치하는 상태이기 때문에 업그레이드 가능
* ② 워커 노드 그룹은 마스터가 업그레이드된 후 업그레이드 가능
* ③ 마스터와 모든 워커 노드 그룹의 버전이 일치해야 업그레이드 가능
* ④ 마스터가 업그레이드됐기 때문에 업그레이드 가능
* ⑤ NHN Cloud에서 지원하는 가장 최신 버전을 사용하고 있기 때문에 업그레이드 불가능


##### 마스터 구성 요소 업그레이드
NHN Cloud의 Kubernetes 클러스터 마스터는 고가용성 보장을 위해 다수의 마스터로 구성되어 있습니다. 마스터에 대해 롤링 업데이트 방식으로 업그레이드되기 때문에 클러스터의 가용성이 보장됩니다. 

이 과정에서 아래와 같은 일들이 발생할 수 있습니다.

* Kubernetes API가 일시적으로 실패할 수 있습니다.


##### 워커 구성 요소 업그레이드
워커 노드 그룹 별로 워커 구성 요소를 업그레이드할 수 있습니다. 워커 구성 요소 업그레이드는 다음 순서로 진행됩니다.

1. 클러스터 오토스케일러 기능을 비활성화 합니다.①
2. 해당 워커 노드 그룹에 버퍼 노드② 를 추가합니다.
3. 워커 노드 그룹 내의 모든 워커 노드에 대해 순차적으로 아래 작업을 수행합니다.
    1. 해당 워커 노드에서 동작 중인 파드를 축출하고, 노드를 스케줄 불가능한 상태로 전환합니다.
    2. 워커 구성 요소를 업그레이드합니다.
    3. 노드를 스케줄 가능한 상태로 전환합니다.
4. 버퍼 노드에서 동작 중인 파드를 축출하고 버퍼 노드를 삭제합니다.
5. 클러스터 오토스케일러 기능을 다시 활성화 합니다.①


주석

* ① 이 단계는 업그레이드 기능 시작 전 클러스터 오토스케일러 기능이 활성화 되어 있는 경우에만 유효합니다.
* ② 버퍼 노드란 업그레이드 과정 중 기존 워커 노드에서 축출당한 파드가 다시 스케줄링 가능하도록 생성해놓는 여유 노드를 말합니다. 해당 워커 노드 그룹에서 정의한 워커 노드와 동일한 규격의 노드로 생성되며, 업그레이드 과정이 종료될 때 자동으로 삭제됩니다. 이 노드는 Instance 요금 정책에 따라 비용이 청구됩니다. 

이 과정에서 아래와 같은 일들이 발생할 수 있습니다.

* 서비스 중인 파드가 축출되어 다른 노드로 스케줄링 됩니다(파드 축출에 대한 더 자세한 내용은 아래 파드 축출 관련 유의 사항을 참고하시길 바랍니다).
* 오토스케일러 기능이 동작하지 않습니다. 


> [파드 축출 관련 유의 사항]
> 1. 데몬셋(daemonset) 컨트롤러에 의한 파드는 축출되지 않습니다.
> 데몬셋 컨트롤러는 각 워커 노드 별로 파드를 실행하기 떄문에 데몬셋 컨트롤러에 의해 실행된 파드는 축출되더라도 다른 노드에서 실행될 수 없습니다. 워커 노드 그룹 업그레이드 과정에서 데몬셋 컨트롤러에 의해 실행된 파드는 축출하지 않습니다. 
> 2. 로컬 저장 공간을 사용하는 파드는 축출되면서 사용하던 데이터를 잃게 됩니다.
> `emptyDir`을 이용해 노드의 로컬 저장 공간을 사용하는 파드는 축출되면서 사용하던 데이터를 잃게 됩니다. 노드의 로컬에 저장된 저장 공간이 다른 노드로 옮겨갈 수 없기 때문입니다. 
> 3. 다른 노드로 복제가 불가능한 파드는 다른 노드로 옮겨지지 않습니다.
> 리플리케이션 컨트롤러(ReplicationController), 레플리카셋(ReplicaSet), 잡(Job), 데몬셋(Daemonset), 스테이트풀(StatefulSet)와 같은 컨트롤러에 의해 실행된 파드가 축출되면 컨트롤러에 의해 다른 노드로 스케줄링 됩니다. 하지만 이와 같은 컨트롤러를 이용하지 않은 파드는 축출된 후 다른 노드로 스케줄링되지 않습니다. 
> 4. PodDisruptionBudgets(PDB) 설정에 의해 축출에 실패하거나 느려질 수 있습니다.
> PodDisruptionBudgets(PDB) 설정으로 유지해야 할 파드 수를 정의할 수 있습니다. 이 기능 설정으로 인해 업그레이드 과정에서 파드 축출이 불가능할 수도 있고, 파드 축출 시간이 길어질 수 있습니다. 파드 축출에 실패하면 업그레이드가 실패합니다. 따라서 PDB 설정이 되어 있는 경우 적절한 PDB 설정으로 파드 축출이 원활히 동작할 수 있도록 설정해야 합니다. PDB 설정에 대한 더 자세한 내용은 [여기](https://kubernetes.io/docs/tasks/run-application/configure-pdb/)를 참고하세요.


안전한 파드 축출에 대한 좀 더 상세한 설명은 [Safely Drain a Node](https://kubernetes.io/docs/tasks/administer-cluster/safely-drain-node/)를 참고하세요

##### 시스템 파드 업그레이드
마스터와 모든 워커 노드 그룹을 업그레이드하여 버전이 일치하게 되면 Kubernetes 클러스터 구성을 위해 동작하는 시스템 파드가 업그레이드 됩니다.

> [주의]
> 마스터 업그레이드 후 워커 노드 그룹을 업그레이드하지 않으면 일부 파드가 정상적으로 동작하지 않을 수 있습니다.

#### 지원 버전
NHN Cloud Kubernetes 서비스는 아래 버전을 지원합니다. 

* v1.17.6
* v1.18.19


## LoadBalancer 서비스
Kubernetes 애플리케이션의 기본 실행 단위인 파드(pod)는 CNI(Container Network Interface)로 클러스터 네트워크에 연결됩니다. 기본적으로 클러스터 외부에서 파드로는 접근할 수 없습니다. 파드의 서비스를 클러스터 외부에 공개하려면 Kubernetes의 `LoadBalancer` 서비스(Service) 객체(object)를 이용해 외부에 공개할 경로를 만들어야 합니다. LoadBalancer 서비스 객체를 만들면 클러스터 외부에 NHN Cloud Load Balancer가 생성되어 서비스 객체와 연결됩니다.

### 웹 서버 파드 생성
다음과 같이 2개의 nginx 파드를 실행하는 디플로이먼트(deployment) 객체 매니페스트 파일을 작성하고 객체를 생성합니다.

```yaml
# nginx.yaml
apiVersion: apps/v1
kind: Deployment
metadata:
  name: nginx-deployment
  labels:
    app: nginx
spec:
  replicas: 2
  selector:
    matchLabels:
      app: nginx
  template:
    metadata:
      labels:
        app: nginx
    spec:
      containers:
      - name: nginx
        image: nginx:1.14.2
        ports:
        - containerPort: 80
```

디플로이먼트 객체를 생성하면 매니페스트에 정의한 파드가 자동으로 생성됩니다.

```
$ kubectl apply -f nginx.yaml
deployment.apps/nginx-deployment created

$ kubectl get pods
NAME                                READY   STATUS    RESTARTS   AGE  
nginx-deployment-7fd6966748-pvrzs   1/1     Running   0          4m13s
nginx-deployment-7fd6966748-wv7rd   1/1     Running   0          4m13s
```

만약 NHN Cloud Container Registry에 저장한 이미지를 사용하고 싶다면 먼저 사용자 레지스트리에 로그인하기 위한 시크릿(secret)을 만들어야 합니다.

```
$ kubectl create secret docker-registry registry-credential --docker-server={사용자 레지스트리 주소} --docker-username={NHN Cloud 계정 email 주소} --docker-password={서비스 Appkey 또는 통합 Appkey}
secret/registry-credential created

$ kubectl get secrets
NAME                  TYPE                             DATA   AGE
registry-credential   kubernetes.io/dockerconfigjson   1      30m
```

디플로이먼트 매니페스트 파일에 시크릿 정보를 추가하고, 이미지 이름을 변경하면 사용자 레지스트리에 저장된 이미지를 이용해 파드를 만들 수 있습니다.

```yaml
# nginx.yaml
...
spec:
  ...
  template:
    ...
    spec:
      containers:
      - name: nginx
        image: {사용자 레지스트리 주소}/nginx:1.14.2
        ...
      imagePullSecrets:
      - name: regcred

```

> [참고]
> NHN Cloud Container Registry 사용 방법은 [Container Registry 사용 가이드](/Container/Container%20Registry/ko/user-guide) 문서를 참고하세요.

### LoadBalancer 서비스 생성
Kubernetes의 서비스 객체를 정의하려면 다음과 같은 항목으로 구성된 매니페스트가 필요합니다.

| 항목 | 설명 |
| --- | --- |
| metadata.name | 서비스 객체의 이름 |
| spec.selector | 서비스 객체와 연결할 파드 이름 |
| spec.ports | 외부 로드 밸런서에서 들어오는 트래픽을 파드에 전달할 인터페이스 설정 |
| spec.ports.name | 인터페이스 이름 |
| spec.ports.protocol | 인터페이스에서 사용할 프로토콜(예: TCP) |
| spec.ports.port | 서비스 객체 외부에 공개할 포트 번호 |
| spec.ports.targetPort | 서비스 객체와 연결할 파드의 포트 번호 |
| spec.type | 서비스 객체 유형 |

다음과 같이 서비스 매니페스트를 작성합니다. 이 LoadBalancer 서비스 객체는 **spec.selector**에 정의된 이름에 따라 `app: nginx` 레이블이 붙은 파드와 연결됩니다. 그리고 **spec.ports**에 정의된 대로 TCP/8080 포트로 들어온 트래픽을 파드의 TCP/80 포트로 전달합니다.

```yaml
# service.yaml
apiVersion: v1
kind: Service
metadata:
  name: nginx-svc
  labels:
    app: nginx
spec:
  ports:
  - port: 8080
    targetPort: 80
    protocol: TCP
  selector:
    app: nginx
  type: LoadBalancer
```

LoadBalancer 서비스 객체를 생성하면 클러스터 외부에 로드 밸런서를 만들고 연결하기까지 약간의 시간이 필요합니다. 외부 로드 밸런서와 연결되기 전에는 **EXTERNAL-IP** 항목이 `<pending>`으로 표시됩니다.

```
$ kubectl apply -f service.yaml
service/nginx-svc created

$ kubectl get service
NAME         TYPE           CLUSTER-IP      EXTERNAL-IP   PORT(S)          AGE
nginx-svc    LoadBalancer   10.254.134.18   <pending>     8080:30013/TCP   11s
```

외부 로드 밸런서와 연결되면 **EXTERNAL-IP** 항목에 IP가 표시됩니다. 이 IP는 외부 로드 밸런서의 플로팅 IP입니다.

```
$ kubectl get service
NAME         TYPE           CLUSTER-IP      EXTERNAL-IP      PORT(S)          AGE
nginx-svc    LoadBalancer   10.254.134.18   123.123.123.30   8080:30013/TCP   3m13s
```

> [참고]
> 생성된 로드 밸런서는 **Network > Load Balancer** 페이지에서 확인할 수 있습니다.
> 로드 밸런서의 IP는 외부에서 접근할 수 있는 플로팅 IP입니다. **Network > Floating IP** 페이지에서 확인할 수 있습니다.


### 인터넷을 통한 서비스 테스트
로드 밸런서에 부착한 플로팅 IP로 HTTP 요청을 보내 Kubernetes 클러스터의 웹 서버 파드가 응답하는지 확인합니다. 서비스 객체의 TCP/8080 포트를 파드의 TCP/80 포트와 연결하도록 설정했기 때문에 TCP/8080 포트로 요청을 보내야 합니다. 외부 로드 밸런서와 서비스 객체, 파드가 잘 연결되었다면 웹 서버는 nginx 기본 페이지를 응답합니다.

```
$ curl http://123.123.123.30:8080
<!DOCTYPE html>
<html>
<head>
<title>Welcome to nginx!</title>
<style>
    body {
        width: 35em;
        margin: 0 auto;
        font-family: Tahoma, Verdana, Arial, sans-serif;
    }
</style>
</head>
<body>
<h1>Welcome to nginx!</h1>
<p>If you see this page, the nginx web server is successfully installed and
working. Further configuration is required.</p>

<p>For online documentation and support please refer to
<a href="http://nginx.org/">nginx.org</a>.<br/>
Commercial support is available at
<a href="http://nginx.com/">nginx.com</a>.</p>

<p><em>Thank you for using nginx.</em></p>
</body>
</html>
```


## 인그레스 컨트롤러
인그레스 컨트롤러(ingress controller)는 인그레스(Ingress) 객체에 정의된 규칙을 참조하여 클러스터 외부에서 내부 서비스로 HTTP와 HTTPS 요청을 라우팅하고 SSL/TSL 종료, 가상 호스팅 등을 제공합니다. 인그레스 컨트롤러와 인그레스에 대한 자세한 내용은 [인그레스 컨트롤러](https://kubernetes.io/ko/docs/concepts/services-networking/ingress-controllers/), [인그레스](https://kubernetes.io/ko/docs/concepts/services-networking/ingress/) 문서를 참고하세요.


### NGINX Ingress Controller 설치
NGINX Ingress Controller는 많이 사용되는 인그레스 컨트롤러 중 하나입니다. 자세한 내용은 [NGINX Ingress Controller](https://kubernetes.github.io/ingress-nginx/)와 [NGINX Ingress Controller for Kubernetes](https://www.nginx.com/products/nginx-ingress-controller/) 문서를 참고하세요.

NGINX Ingress Controller는 필요한 자원을 바로 생성할 수 있도록 미리 정의한 매니페스트 파일을 제공합니다. 이 매니페스트를 이용하면 쉽게 필요한 자원을 생성할 수 있습니다.

```
$ kubectl apply -f https://raw.githubusercontent.com/kubernetes/ingress-nginx/nginx-0.30.0/deploy/static/mandatory.yaml
namespace/ingress-nginx created
configmap/nginx-configuration created
configmap/tcp-services created
configmap/udp-services created
serviceaccount/nginx-ingress-serviceaccount created
clusterrole.rbac.authorization.k8s.io/nginx-ingress-clusterrole created
role.rbac.authorization.k8s.io/nginx-ingress-role created
rolebinding.rbac.authorization.k8s.io/nginx-ingress-role-nisa-binding created
clusterrolebinding.rbac.authorization.k8s.io/nginx-ingress-clusterrole-nisa-binding created
deployment.apps/nginx-ingress-controller created
limitrange/ingress-nginx created
```

### LoadBalancer 서비스 생성
인그레스 컨트롤러 역시 파드로 생성되기 때문에 외부에 공개하기 위해서는 LoadBalancer 서비스 또는 NodePort 서비스를 만들어야 합니다. 다음과 같이 HTTP와 HTTPS를 처리할 수 있는 LoadBalancer 서비스 매니페스트를 정의합니다.

```yaml
# ingress-nginx-lb.yaml
apiVersion: v1
kind: Service
metadata:
  name: ingress-nginx
  namespace: ingress-nginx
  labels:
    app.kubernetes.io/name: ingress-nginx
    app.kubernetes.io/part-of: ingress-nginx
spec:
  type: LoadBalancer
  selector:
    app.kubernetes.io/name: ingress-nginx
    app.kubernetes.io/part-of: ingress-nginx
  ports:
    - name: http
      port: 80
      targetPort: 80
      protocol: TCP
    - name: https
      port: 443
      targetPort: 443
      protocol: TCP
  selector:
    app.kubernetes.io/name: ingress-nginx
    app.kubernetes.io/part-of: ingress-nginx
```

서비스 객체를 생성하고 외부 로드 밸런서가 연결되어 있는지 확인합니다. **EXTERNAL-IP** 필드에는 플로팅 IP 주소가 설정되어 있어야 합니다.

```
$ kubectl apply -f ingress-nginx-lb.yaml
service/ingress-nginx created

$ kubectl get svc -n ingress-nginx
NAME            TYPE           CLUSTER-IP     EXTERNAL-IP      PORT(S)                      AGE
ingress-nginx   LoadBalancer   10.254.2.128   123.123.123.41   80:30820/TCP,443:30269/TCP   39s
```

### URI 기반 서비스 분기
인그레스 컨트롤러는 URI를 기반으로 서비스를 분기할 수 있습니다. 아래 그림은 URI를 기반으로 서비스를 분기하는 간단한 예제의 구조를 나타냅니다.

![ingress-01.png](http://static.toastoven.net/prod_infrastructure/container/kubernetes/ingress-01.png)

#### 서비스와 파드 생성
다음과 같이 서비스와 파드를 생성하기 위한 매니페스트를 작성합니다. `tea-svc` 서비스에는 `tea` 파드를 연결하고, `coffee-svc` 서비스에는 `coffee` 파드를 연결합니다.

```yaml
# cafe.yaml
apiVersion: apps/v1
kind: Deployment
metadata:
  name: coffee
spec:
  replicas: 3
  selector:
    matchLabels:
      app: coffee
  template:
    metadata:
      labels:
        app: coffee
    spec:
      containers:
      - name: coffee
        image: nginxdemos/nginx-hello:plain-text
        ports:
        - containerPort: 8080
---
apiVersion: v1
kind: Service
metadata:
  name: coffee-svc
spec:
  ports:
  - port: 80
    targetPort: 8080
    protocol: TCP
    name: http
  selector:
    app: coffee
---
apiVersion: apps/v1
kind: Deployment
metadata:
  name: tea
spec:
  replicas: 2
  selector:
    matchLabels:
      app: tea
  template:
    metadata:
      labels:
        app: tea
    spec:
      containers:
      - name: tea
        image: nginxdemos/nginx-hello:plain-text
        ports:
        - containerPort: 8080
---
apiVersion: v1
kind: Service
metadata:
  name: tea-svc
  labels:
spec:
  ports:
  - port: 80
    targetPort: 8080
    protocol: TCP
    name: http
  selector:
    app: tea
```

매니페스트를 적용하고 디플로이먼트, 서비스, 파드가 생성되었는지 확인합니다. 파드는 **Running** 상태여야 합니다.

```
$ kubectl apply -f cafe.yaml
deployment.apps/coffee created
service/coffee-svc created
deployment.apps/tea created
service/tea-svc created

$ kubectl get deploy,svc,pods
NAME                           READY   UP-TO-DATE   AVAILABLE   AGE
deployment.extensions/coffee   3/3     3            3           18s
deployment.extensions/tea      2/2     2            2           18s

NAME                 TYPE        CLUSTER-IP       EXTERNAL-IP   PORT(S)   AGE
service/coffee-svc   ClusterIP   10.254.51.117    <none>        80/TCP    18s
service/tea-svc      ClusterIP   10.254.210.170   <none>        80/TCP    18s

NAME                          READY   STATUS    RESTARTS   AGE
pod/coffee-67c6f7c5fd-98vh5   1/1     Running   0          18s
pod/coffee-67c6f7c5fd-c58l2   1/1     Running   0          18s
pod/coffee-67c6f7c5fd-dmxf6   1/1     Running   0          18s
pod/tea-7df475c6-gtlx5        1/1     Running   0          18s
pod/tea-7df475c6-lxqsx        1/1     Running   0          18s
```

#### 인그레스(Ingress) 생성
요청 경로에 따라 서비스를 연결하는 인그레스 매니페스트를 작성합니다. 엔드포인트가 `/tea`인 요청은 `tea-svc` 서비스에 연결하고 `/coffee`인 요청은 `coffee-svc` 서비스에 연결합니다.

```yaml
# cafe-ingress-uri.yaml
apiVersion: extensions/v1beta1
kind: Ingress
metadata:
  name: cafe-ingress-uri
spec:
  rules:
  - http:
      paths:
      - path: /tea
        backend:
          serviceName: tea-svc
          servicePort: 80
      - path: /coffee
        backend:
          serviceName: coffee-svc
          servicePort: 80
```

인그레스를 생성하고 잠시 후 확인했을 때 **ADDRESS** 필드에 IP가 설정되어 있어야 합니다.

```
$ kubectl apply -f cafe-ingress-uri.yaml
ingress.extensions/cafe-ingress-uri created

$ kubectl get ingress cafe-ingress-uri
NAME               HOSTS   ADDRESS          PORTS   AGE
cafe-ingress-uri   *       123.123.123.44   80      88s
```

#### HTTP 요청 전송
외부 호스트에서 ingress의 **ADDRESS** 필드에 설정된 IP 주소로 HTTP 요청을 전송해 인그레스가 올바르게 설정되었는지 확인합니다.

엔드포인트 `/coffee`에 대한 요청은 `coffee-svc` 서비스에 전달되어 `coffee` 파드가 응답합니다. 응답의 **Server name** 항목을 보면 `coffee` 파드들이 라운드-로빈 방식으로 번갈아 응답하는 것을 확인할 수 있습니다.

```
$ curl http://123.123.123.44/coffee
Server address: 10.100.3.48:8080
Server name: coffee-67c6f7c5fd-c58l2
Dat#e: 07/Apr/2020:08:24:27 +0000
URI: /coffee
Request ID: e831901e441303ad59fb02214c49d84a

$ curl http://123.123.123.44/coffee
Server address: 10.100.2.23:8080
Server name: coffee-67c6f7c5fd-98vh5
Date: 07/Apr/2020:08:24:28 +0000
URI: /coffee
Request ID: e78427e68a1cd61ec633b9328359874e
```

마찬가지로 엔드포인트 `/tea`에 대한 요청은 `tea-svc` 서비스에  전달되어 `tea` 파드가 응답합니다.

```
$ curl http://123.123.123.44/tea
Server address: 10.100.2.24:8080
Server name: tea-7df475c6-lxqsx
Date: 07/Apr/2020:08:25:03 +0000
URI: /tea
Request ID: 59303a5a5baa60802b463b1856c8ce8d
```

정의되지 않은 URI로 요청을 보내면 인그레스 컨트롤러가 `404 Not Found`를 응답합니다.

```
$ curl http://123.123.123.44/
<html>
<head><title>404 Not Found</title></head>
<body>
<center><h1>404 Not Found</h1></center>
<hr><center>nginx/1.17.8</center>
</body>
</html>
```

#### 리소스 삭제
테스트에 사용한 자원들은 생성할 때 사용한 매니페스트를 이용해 삭제할 수 있습니다.

```
$ kubectl delete -f cafe-ingress-uri.yaml
ingress.extensions "cafe-ingress-uri" deleted

$ kubectl delete -f cafe.yaml
deployment.apps "coffee" deleted
service "coffee-svc" deleted
deployment.apps "tea" deleted
service "tea-svc" deleted
```

### 호스트 기반 서비스 분기
인그레스 컨트롤러는 호스트 이름을 기반으로 서비스를 분기할 수 있습니다. 아래 그림은 호스트 이름을 기반으로 서비스를 분기하는 간단한 예제의 구조를 나타냅니다.

![ingress-02.png](http://static.toastoven.net/prod_infrastructure/container/kubernetes/ingress-02.png)

#### 서비스와 파드 생성
[URI 기반 서비스 분기](/Container/Kubernetes/ko/user-guide/#uri)와 동일한 매니페스트를 이용해 서비스와 파드를 생성합니다.

#### 인그레스 생성
호스트 이름에 따라 서비스를 연결하는 인그레스 매니페스트를 작성합니다. `tea.cafe.example.com` 호스트로 들어온 요청은 `tea-svc` 서비스에 연결하고 `coffee.cafe.example.com` 호스트로 들어온 요청은 `coffee-svc` 서비스에 연결합니다.

```yaml
# cafe-ingress-host.yaml
apiVersion: extensions/v1beta1
kind: Ingress
metadata:
  name: cafe-ingress-host
spec:
  rules:
  - host: tea.cafe.example.com
    http:
      paths:
      - path: /
        backend:
          serviceName: tea-svc
          servicePort: 80
  - host: coffee.cafe.example.com
    http:
      paths:
      - path: /
        backend:
          serviceName: coffee-svc
          servicePort: 80
```

인그레스를 생성하고 잠시 후 확인했을 때 **ADDRESS** 필드에 IP가 설정되어 있어야 합니다.

```
$ kubectl apply -f cafe-ingress-host.yaml
ingress.extensions/cafe-ingress-host created

$ kubectl get ingress
NAME                HOSTS                                          ADDRESS          PORTS   AGE
cafe-ingress-host   tea.cafe.example.com,coffee.cafe.example.com   123.123.123.44   80      4m29s
```

#### HTTP Request 전송
외부 호스트에서 인그레스의 ADDRESS에 설정된 IP로 HTTP 요청을 전송합니다. 다만 호스트 이름을 이용해 서비스를 분기하도록 인그레스를 구성했기 때문에 호스트 이름을 이용해 요청을 전송해야 합니다.

> [참고]
> 임의의 호스트 이름을 사용하여 테스트하려면 curl의 --resolve 옵션을 사용합니다. --resolve 옵션은 `{호스트 이름}:{포트 번호}:{IP}` 형식으로 입력합니다. 이는 {호스트 이름}으로 보내는 {포트번호}에 대한 요청을 {IP}로 해석(resolve)하라는 의미입니다.
> `/etc/host` 파일을 열어 `{IP} {호스트 이름}` 형식으로 추가할 수도 있습니다.

호스트 `coffee.cafe.example.com`로 요청을 전송하면 `coffee-svc` 서비스에 전달되어 `coffee` 파드가 응답합니다.

```
$ curl --resolve coffee.cafe.example.com:80:123.123.123.44 http://coffee.cafe.example.com/
Server address: 10.100.2.25:8080
Server name: coffee-67c6f7c5fd-2bbzf
Date: 07/Apr/2020:08:45:39 +0000
URI: /
Request ID: 29fd8a244b9f0a5ff5f35d1dc35edccf
```

호스트 `tea.cafe.example.com`로 요청을 전송하면 `tea-svc` 서비스에 전달되어 `tea` 파드가 응답합니다.

```
$ curl --resolve tea.cafe.example.com:80:123.123.123.44 http://tea.cafe.example.com/
Server address: 10.100.3.52:8080
Server name: tea-7df475c6-q8mdx
Date: 07/Apr/2020:08:53:44 +0000
URI: /
Request ID: fe61c1589d3ab8ef4ca4507245251ef3
```

알려지지 않은 호스트로 요청을 보내면 인그레스 컨트롤러가 `404 Not Found`를 응답합니다.

```
$ curl http://123.123.123.44
<html>
<head><title>404 Not Found</title></head>
<body>
<center><h1>404 Not Found</h1></center>
<hr><center>nginx/1.17.8</center>
</body>
</html>

$ curl --resolve test.example.com:80:123.123.123.44 http://test.example.com/
<html>
<head><title>404 Not Found</title></head>
<body>
<center><h1>404 Not Found</h1></center>
<hr><center>nginx/1.17.8</center>
</body>
</html>
```

## Kubernetes 대시보드
NHN Cloud Kubernetes 서비스는 기본 웹 UI 대시보드(dashboard)를 제공합니다. Kubernetes 대시보드에 대한 자세한 내용은 [웹 UI (대시보드)](https://kubernetes.io/ko/docs/tasks/access-application-cluster/web-ui-dashboard/) 문서를 참고하세요.

### 대시보드 서비스 공개
사용자 Kubernetes에는 대시보드를 공개하기 위한 `kubernetes-dashboard` 서비스 객체가 미리 생성되어 있습니다.

```
$ kubectl get svc kubernetes-dashboard -n kube-system
NAME                   TYPE        CLUSTER-IP      EXTERNAL-IP   PORT(S)   AGE
kubernetes-dashboard   ClusterIP   10.254.95.176   <none>        443/TCP   2d4h

$ kubectl describe svc kubernetes-dashboard -n kube-system
Name:              kubernetes-dashboard
Namespace:         kube-system
Labels:            k8s-app=kubernetes-dashboard
Annotations:       kubectl.kubernetes.io/last-applied-configuration:
                     {"apiVersion":"v1","kind":"Service","metadata":{"annotations":{},"labels":{"k8s-app":"kubernetes-dashboard"},"name":"kubernetes-dashboard"...
Selector:          k8s-app=kubernetes-dashboard
Type:              ClusterIP
IP:                10.254.95.176
Port:              <unset>  443/TCP
TargetPort:        8443/TCP
Endpoints:         10.100.2.3:8443
Session Affinity:  None
Events:
...
```

그러나 `kubernetes-dashboard` 서비스 객체는 ClusterIP 유형이기 때문에 아직 클러스터 외부에 공개되어 있지 않습니다. 대시보드를 외부 공개하려면 서비스 객체를 LoadBalancer 유형으로 변경하거나 인그레스 컨트롤러와 인그레스 객체를 생성해야 합니다.

#### LoadBalancer 서비스 객체로 변경

`LoadBalancer` 유형으로 서비스 객체를 변경하면 클러스터 외부에 NHN Cloud Load Balancer가 생성되고, 로드 밸런서와 서비스 객체와 연결됩니다. 로드 밸런서와 연결된 서비스 객체를 조회하면 **EXTERNAL-IP** 필드에 로드 밸런서의 IP가 표시됩니다. `LoadBalancer` 유형의 서비스 객체에 대한 설명은 [LoadBalancer 서비스](/Container/Kubernetes/ko/user-guide/#loadbalancer)를 참고하세요. 아래 그림은 `LoadBalancer` 유형의 서비스를 이용해 대시보드를 외부에 공개하는 구조를 나타냅니다.

![dashboard-01.png](http://static.toastoven.net/prod_infrastructure/container/kubernetes/dashboard-01.png)

다음과 같이 `kubernetes-dashboard` 서비스 객체의 유형을 `LoadBalancer`로 변경합니다.

```
$ kubectl -n kube-system patch svc/kubernetes-dashboard -p '{"spec":{"type":"LoadBalancer"}}'
service/kubernetes-dashboard patched
```

`kubernetes-dashboard` 서비스 객체가 `LoadBalancer` 유형으로 변경되면 잠시 후 **EXTERNAL-IP** 필드에서 로드 밸런서 IP를 확인할 수 있습니다.

```
$ kubectl get svc -n kube-system
NAME                   TYPE           CLUSTER-IP      EXTERNAL-IP      PORT(S)                  AGE
...
kubernetes-dashboard   LoadBalancer   10.254.95.176   123.123.123.81   443:30963/TCP            2d23h
```

> [참고]
> 생성된 로드 밸런서는 **Network > Load Balancer** 페이지에서 확인할 수 있습니다.
> 로드 밸런서의 IP는 외부에서 접근할 수 있는 플로팅 IP입니다. **Network > Floating IP** 페이지에서 확인할 수 있습니다.

웹 브라우저에서 `https://{EXTERNAL-IP}`로 접속하면 Kubernetes 대시보드 페이지가 로딩됩니다. 로그인을 위해 필요한 토큰은 [대시보드 엑세스 토큰](/Container/Kubernetes/ko/user-guide/#_23)을 참고하세요.

> [참고]
> Kubernetes 대시보드는 자동 생성되는 사설 인증서를 사용하기 때문에 웹 브라우저의 종류와 보안 설정에 따라 안전하지 않은 페이지로 표시될 수 있습니다.

#### 인그레스(Ingress)를 이용한 서비스 공개

인그레스는 클러스터 내부의 여러 서비스들로 접근하기 위한 라우팅을 제공하는 네트워크 객체입니다. 인그레스 객체의 설정은 인그래스 컨트롤러로 구동됩니다. `kubernetes-dashboard` 서비스 객체를 인그레스를 통해 공개할 수 있습니다. 인그레스와 인그레스 컨트롤러에 대한 설명은 [인그레스 컨트롤러](/Container/Kubernetes/ko/user-guide/#_16)를 참고하세요. 아래 그림은 인그레스를 통해 대시보드를 외부에 공개하는 구조를 나타냅니다.

![dashboard-02.png](http://static.toastoven.net/prod_infrastructure/container/kubernetes/dashboard-02.png)

[NGINX Ingress Controller 설치](/Container/Kubernetes/ko/user-guide/#nginx-ingress-controller)를 참고해 `NGINX Ingress Controller`를 설치하고 `LoadBalancer` 유형의 서비스를 생성합니다. 그리고 다음과 같이 인그레스 객체 생성을 위한 매니페스트를 작성합니다.

```yaml
# kubernetes-dashboard-ingress-tls-passthrough.yaml
apiVersion: extensions/v1beta1
kind: Ingress
metadata:
  name: k8s-dashboard-ingress
  namespace: kube-system
  annotations:
    ingress.kubernetes.io/ssl-passthrough: "true"
    kubernetes.io/ingress.allow-http: "false"
    kubernetes.io/ingress.class: nginx
    nginx.ingress.kubernetes.io/backend-protocol: HTTPS
    nginx.ingress.kubernetes.io/proxy-body-size: 100M
    nginx.ingress.kubernetes.io/rewrite-target: /
    nginx.org/ssl-backend: kubernetes-dashboard
spec:
  rules:
  - http:
      paths:
      - backend:
          serviceName: kubernetes-dashboard
          servicePort: 443
        path: /
  tls:
  - secretName: kubernetes-dashboard-certs
```

매니페스트를 적용해 인그레스를 생성하고 `ingress-nginx` 서비스 객체의 **EXTERNAL-IP** 필드를 확인합니다.

```
$ kubectl apply -f kubernetes-dashboard-ingress-tls-passthrough.yaml
ingress.extensions/k8s-dashboard-ingress created

$ kubectl get service/ingress-nginx -n ingress-nginx
NAME            TYPE           CLUSTER-IP       EXTERNAL-IP      PORT(S)                      AGE
ingress-nginx   LoadBalancer   10.254.211.113   123.123.123.29   80:32680/TCP,443:31631/TCP   19h
```

웹 브라우저에서 `https://{EXTERNAL-IP}`로 접속하면 Kubernetes 대시보드 페이지가 로딩됩니다. 로그인을 위해 필요한 토큰은 [대시보드 엑세스 토큰](/Container/Kubernetes/ko/user-guide/#_23)을 참고하세요.

### 대시보드 엑세스 토큰
Kubernetes 대시보드에 로그인하려면 토큰이 필요합니다. 토큰은 다음 명령으로 얻을 수 있습니다.

```
# SECRET_NAME=$(kubectl -n kube-system get secrets | grep "kubernetes-dashboard-token" | cut -f1 -d ' ')

$ kubectl describe secret $SECRET_NAME -n kube-system | grep -E '^token' | cut -f2 -d':' | tr -d " "
eyJhbGc...-QmXA
```

출력된 토큰을 브라우저의 토큰 입력 창에 입력하면 클러스터 관리자 권한을 부여받은 사용자로 로그인할 수 있습니다.


## 퍼시스턴트 볼륨
퍼시스턴트 볼륨(Persistent Volume, PV)는 물리 저장 장치(volume)를 표현하는 Kubernetes의 자원입니다. 하나의 PV는 하나의 NHN Cloud Block Storage와 연결됩니다. 자세한 내용은 [퍼시스턴트 볼륨](https://kubernetes.io/ko/docs/concepts/storage/persistent-volumes/) 문서를 참고하세요.

PV를 파드에 연결해 사용하려면 퍼시스턴트 볼륨 클레임(Persistent Volume Claims, PVC) 객체가 필요합니다. PVC는 용량, 읽기/쓰기 모드 등 필요한 볼륨의 요구 사항을 정의합니다.

PV와 PVC로 사용자는 사용하고 싶은 볼륨의 속성을 정의하고, 시스템은 사용자의 요구 사항에 맞는 볼륨 리소스를 할당하는 방식으로 자원의 사용과 관리를 분리합니다.

### PV/PVC의 생명 주기
PV와 PVC는 4단계의 생명 주기(life cycle)를 따릅니다.

* 프로비저닝(provisioning)
사용자가 직접 볼륨을 확보하고 PV를 생성(static provisioning)하거나 [스토리지 클래스](https://kubernetes.io/ko/docs/concepts/storage/storage-classes/)를 사용해 동적으로 생성(dynamic provisioning)할 수 있습니다.

* 바인딩(binding)
PV와 PVC를 1:1로 바인딩합니다. 동적 프로비저닝으로 PV를 생성했다면 바인딩도 자동으로 수행됩니다.

* 사용(using)
PV를 파드에 마운트해 사용합니다.

* 반환(reclaiming)
사용을 마친 볼륨을 회수합니다. 회수 방법은 삭제(Delete), 보존(Retain), 재사용(Recycle)이 있습니다.

| 방법 | 설명 |
| --- | --- |
| 삭제(Delete) | PV를 삭제할 때 연결된 볼륨을 함께 삭제합니다. |
| 보존(Retain) | PV를 삭제할 때 연결된 볼륨을 삭제하지 않습니다. 볼륨은 사용자가 직접 삭제하거나 재사용 할 수 있습니다. |
| 재사용(Recycle) | PV를 삭제할 때 연결된 볼륨을 삭제하지 않고 재사용할 수 있는 상태로 만듭니다. 이 방법은 사용 중단(deprecated) 되었습니다. |


### 정적 프로비저닝

정적 프로비저닝(static provisioning)은 사용자가 직접 블록 스토리지를 준비해야 합니다. NHN Cloud 웹 콘솔의 **Storage > Block Storage** 서비스 페이지에서 **블록 스토리지 생성** 버튼을 클릭해 PV와 연결할 블록 스토리지를 생성합니다. 블록 스토리지 가이드의 [블록 스토리지 생성](/Storage/Block%20Storage/ko/console-guide/#_0)을 참고하세요.

PV를 생성하려면 블록 스토리지의 ID가 필요합니다. **Storage > Block Storage** 서비스 페이지의 블록 스토리지 목록에서 사용할 블록 스토리지를 선택합니다. 하단 **정보** 탭의 블록 스토리지 이름 항목에서 ID를 확인할 수 있습니다.

> [주의]
> 블록 스토리지와 파드를 구동할 노드 그룹 인스턴스의 가용성 영역이 같아야 합니다. 가용성 영역이 다르면 연결할 수 없습니다.

스토리지 클래스 매니페스트를 작성합니다. NHN Cloud Block Storage를 사용하려면 **provisioner**를 반드시 `kubernetes.io/cinder`로 설정해야 합니다.

```yaml
# storage_class.yaml
apiVersion: storage.k8s.io/v1
kind: StorageClass
metadata:
  name: sc-default
provisioner: kubernetes.io/cinder
```

스토리지 클래스를 생성하고 확인합니다.

```
$ kubectl apply -f storage_class.yaml
storageclass.storage.k8s.io/sc-default created

$ kubectl get sc
NAME         PROVISIONER            AGE
sc-default   kubernetes.io/cinder   8s
```

블록 스토리지와 연결할 PV 매니페스트를 작성합니다. **spec.storageClassName**에는 스토리지 클래스 이름을 입력합니다. NHN Cloud Block Storage를 사용하려면 **spec.accessModes**는 반드시 `ReadWriteOnce`로 설정해야 합니다. **spec.presistentVolumeReclaimPolicy**는 `Delete` 또는 `Retain`으로 설정할 수 있습니다.

```yaml
# pv-static.yaml
apiVersion: v1
kind: PersistentVolume
metadata:
  name: pv-static-001
spec:
  capacity:
    storage: 10Gi
  volumeMode: Filesystem
  accessModes:
    - ReadWriteOnce
  persistentVolumeReclaimPolicy: Delete
  storageClassName: sc-default
  cinder:
    fsType: "ext3"
    volumeID: "e6f95191-d58b-40c3-a191-9984ce7532e5"
```

PV를 생성하고 확인합니다.

```
$ kubectl apply -f pv-static.yaml
persistentvolume/pv-static-001 created

$ kubectl get pv -o wide
NAME            CAPACITY   ACCESS MODES   RECLAIM POLICY   STATUS      CLAIM   STORAGECLASS   REASON   AGE   VOLUMEMODE
pv-static-001   10Gi       RWO            Delete           Available           sc-default              7s    Filesystem
```

생성한 PV를 사용하기 위한 PVC 매니페스트를 작성합니다. **spec.volumeName**에는 PV의 이름을 지정해야 합니다. 다른 항목들은 PV 매니페스트의 내용과 동일하게 설정합니다.

```yaml
# pvc-static.yaml
apiVersion: v1
kind: PersistentVolumeClaim
metadata:
  name: pvc-static
  namespace: default
spec:
  volumeName: pv-static-001
  accessModes:
  - ReadWriteOnce
  resources:
    requests:
      storage: 10Gi
  storageClassName: sc-default
```

PVC를 생성하고 확인합니다.

```
$ kubectl apply -f pvc-static.yaml
persistentvolumeclaim/pvc-static created

$ kubectl get pvc -o wide
NAME         STATUS   VOLUME          CAPACITY   ACCESS MODES   STORAGECLASS   AGE   VOLUMEMODE
pvc-static   Bound    pv-static-001   10Gi       RWO            sc-default     7s    Filesystem
```

PVC를 생성한 다음 PV의 상태를 조회해보면 **CLAIM** 항목에 PVC 이름이 지정되고, **STATUS** 항목이 `Bound`로 변경된 것을 확인할 수 있습니다.

```
$ kubectl get pv -o wide
NAME            CAPACITY   ACCESS MODES   RECLAIM POLICY   STATUS   CLAIM                STORAGECLASS   REASON   AGE   VOLUMEMODE
pv-static-001   10Gi       RWO            Delete           Bound    default/pvc-static   sc-default              79s   Filesystem
```


### 동적 프로비저닝

동적 프로비저닝(dynamic provisioning)은 스토리지 클래스에 정의된 속성을 참조하여 자동으로 블록 스토리지를 생성합니다. 스토리지 클래스 매니페스트의 **parameters.type**에 NHN Cloud Block Storage 유형을 지정할 수 있습니다. 지정하지 않으면 HDD 유형으로 설정됩니다.

| 타입 | 설정값 |
| --- | --- |
| HDD | General HDD |
| SSD | General SSD |

블록 스토리지는 노드 그룹과 같은 가용성 영역(availability zone)에 만들어야 연결할 수 있습니다. 스토리지 클래스 매니페스트의 **parameters.availability**에 블록 스토리지를 생성할 가용성 영역을 지정할 수 있습니다. 연결할 노드 그룹의 가용성 영역은 노드 그룹 목록에서 확인할 수 있습니다.

> [주의]
> 스토리지 클래스 매니페스트에 가용성 영역을 지정하지 않으면 임의의 가용성 영역에 블록 스토리지를 만듭니다. 블록 스토리지가 노드 그룹과 다른 가용성 영역에 생성되면 연결하지 못할 수 있으니 반드시 가용성 영역을 지정해야 합니다.

```yaml
# storage_class.yaml
apiVersion: storage.k8s.io/v1
kind: StorageClass
metadata:
  name: sc-ssd
provisioner: kubernetes.io/cinder
parameters:
  type: General SSD
  availability: kr-pub-a
```

동적 프로비저닝은 PV를 생성할 필요가 없습니다. 따라서 PVC 매니페스트에는 **spec.volumeName**를 설정하지 않습니다.

```yaml
# pvc-dynamic.yaml
apiVersion: v1
kind: PersistentVolumeClaim
metadata:
  name: pvc-dynamic
  namespace: default
spec:
  accessModes:
  - ReadWriteOnce
  resources:
    requests:
      storage: 10Gi
  storageClassName: sc-ssd
```

PVC를 생성하면 PV가 자동으로 생성됩니다. PV에 연결된 블록 스토리지도 자동으로 생성되며 NHN Cloud 웹 콘솔 **Storage > Block Storage** 서비스 페이지의 블록 스토리지 목록에서 확인할 수 있습니다.

```
$ kubectl apply -f pvc-dynamic.yaml
persistentvolumeclaim/pvc-dynamic created

$ kubectl get sc,pv,pvc
NAME                                     PROVISIONER            AGE
storageclass.storage.k8s.io/sc-default   kubernetes.io/cinder   10m

NAME                                                        CAPACITY   ACCESS MODES   RECLAIM POLICY   STATUS   CLAIM                 STORAGECLASS   REASON   AGE
persistentvolume/pvc-c63da3f9-dfcb-4cae-a9a9-67137994febc   10Gi       RWO            Delete           Bound    default/pvc-dynamic   sc-default              16s

NAME                                STATUS   VOLUME                                     CAPACITY   ACCESS MODES   STORAGECLASS   AGE
persistentvolumeclaim/pvc-dynamic   Bound    pvc-c63da3f9-dfcb-4cae-a9a9-67137994febc   10Gi       RWO            sc-default     17s
```

> [주의]
> 동적 프로비저닝으로 생성된 블록 스토리지는 웹 콘솔에서 삭제할 수 없습니다. 또한 클러스터를 삭제할 때 자동으로 삭제되지 않습니다. 따라서 클러스터를 삭제하기 전에 PVC를 모두 삭제해야 합니다. PVC를 삭제하지 않고 클러스터를 삭제하면 과금이 될 수 있습니다. 동적 프로비저닝을 생성된 PVC의 reclaimPolicy는 기본적으로 `Delete`로 설정되기 때문에 PVC만 삭제해도 PV와 블록 스토리지가 삭제됩니다.


### 파드에 PVC 마운트

파드에 PVC를 마운트하려면 파드 매니페스트에 마운트 정보를 정의해야 합니다. `spec.volumes.persistenVolumeClaim.claimName`에 사용할 PVC 이름을 입력합니다. 그리고 `spec.containers.volumeMounts.mountPath`에 마운트할 경로를 입력합니다.

아래 예제는 정적 프로비저닝으로 생성한 PVC를 파드의 `/usr/share/nginx/html`에 마운트합니다.

```yaml
# pod-pvc.yaml
apiVersion: v1
kind: Pod
metadata:
  name: nginx-with-static-pv
spec:
  containers:
    - name: web
      image: nginx
      ports:
        - name: web
          containerPort: 80
          hostPort: 8082
          protocol: TCP
      volumeMounts:
        - name: html-volume
          mountPath: "/usr/share/nginx/html"
  volumes:
    - name: html-volume
      persistentVolumeClaim:
        claimName: pvc-static
```

파드를 생성하고 블록 스토리지가 마운트되어 있는지 확인합니다.

```
$ kubectl apply -f pod-static-pvc.yaml
pod/nginx-with-static-pv created

$ kubectl get pods
NAME                   READY   STATUS    RESTARTS   AGE
nginx-with-static-pv   1/1     Running   0          50s

$ kubectl exec -ti nginx-with-static-pv -- df -h
Filesystem      Size  Used Avail Use% Mounted on
...
/dev/vdc        9.8G   23M  9.7G   1% /usr/share/nginx/html
...
```

NHN Cloud 웹 콘솔 **Storage > Block Storage** 서비스 페이지에서도 블록 스토리지의 연결 정보를 확인할 수 있습니다.
