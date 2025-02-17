## Container > Kubernetes > 릴리스 노트

### 2021. 07. 27.

#### 기능 추가

* 노드 그룹 생성 시 예약 스크립트 기능을 사용할 수 있습니다.
* 워커 노드에 컨테이너 로그 로테이션 설정이 추가되었습니다.
    * 이미지 업데이트
        * CentOS 7.8 - Container (2021.07.27)
    * 컨테이너 로그 관리에 대한 내용은 [문제 해결 가이드](/Container/Kubernetes/ko/troubleshooting-guide)를 참고하세요.

### 2021. 06. 29.

#### 기능 추가

* Kubernetes v1.18.19를 지원합니다.
* 클러스터 버전을 업그레이드할 수 있습니다.

### 2021. 03. 23.

#### 기능 추가

* 사용자 클러스터에서 발생한 이벤트를 NHN CloudTrail에서 확인할 수 있습니다.

#### 버그 수정
* 그래픽 최적화된 인스턴스 타입(g2)으로 노드 그룹 생성 시 정상 초기화되지 않는 문제가 수정되었습니다.

### 2021. 02. 23.

#### 기능 개선
* Kubernetes 승인 컨트롤러(admission controller)에 PodSecurityPolicy 플러그인이 추가되었습니다.
* 클러스터 및 노드 그룹 생성 시 사용하는 이미지의 배포판 버전이 변경되었습니다.
    * 이미지 업데이트
        * CentOS 7.8 - Container (2021.02.23)

### 2021. 01. 26.
#### 버그 수정
* 인터넷 게이트웨이가 연결되지 않은 환경에서 오토 스케일러 기능이 동작하지 않는 문제가 수정되었습니다.
    * 이미지 업데이트
        * CentOS 7.5 - Container (2021.01.26)

### 2020. 12. 29.
#### 기능 개선
* Kubernetes CSR(Certificate Signing Request) 기능을 사용할 수 있습니다.

### 2020. 11. 24.
#### 기능 추가
* 오토 스케일러 기능을 사용할 수 있습니다.

#### 기능 개선
* 클러스터를 삭제할 때 남아있는 로드 밸런서와 플로팅 IP를 삭제합니다.

### 2020. 10. 27.
#### 기능 추가
* Kubernetes 클러스터에서 GPU 기반의 노드 그룹을 사용할 수 있습니다.
    * 이미지 업데이트
        * CentOS 7.5 - Container (2020.10.27)

### 2020. 09. 22.
#### 기능 개선
* 동작 중인 노드 그룹에 노드를 추가하거나 삭제할 수 있습니다. 

#### 신규 서비스 출시
* 한국(평촌) 리전에서도 Kubernetes 서비스를 사용할 수 있습니다.

### 2020. 08. 25.
#### 기능 개선
* 콘솔에서 Kubernetes 클러스터를 생성할 때, 임의의 영역(zone)을 선택할 수 있습니다.

### 2020. 06. 23.
#### 신규 서비스 출시
* 콘솔에서 Kubernetes 클러스터를 생성하고 관리할 수 있습니다.
