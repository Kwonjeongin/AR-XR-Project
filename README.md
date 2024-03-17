# AR-XR-Project
AR-XRProject는 ARNavigation 및 XR 컨텐츠를 개발하는 프로젝트 입니다. 
<br>
사용자가 지역을 걸어다니며 이용할 수 있는 ARNavigation 및 특정 위치에서 상호작용할 수 있는 AR도슨트를 포함합니다.
<br>
<br>
![ezgif-1-eb3981f90d](https://github.com/henry2craftman/ARNavigation/assets/141684228/27f395b6-70f9-41b1-ad73-484e9786abc7)


---
<br>

## 상태 및 전제조건
> Unity Version: 2022.3.2f1

> Platform: Android

>API : Google Map Api 

> 지원기기: [ARCore 지원 기기](https://developers.google.com/ar/devices?hl=ko, "ARCore 지원 기기")

---
## 기능소개 
0. Unity 이해
1. AR 내비게이션
2. AR 도슨트 체험존
---
## 기능상세 소개

### 1. AR 내비게이션 
Google API 기반 Navigation

### 2. AR 도슨트 체험존 

[ImageDetection]
- AR Core의 AR Tracked Image Manager를 사용하여 Reference Image Library에 등록된 도슨트 정보 이미지 감지 
- 각 Logo를 인식했을 때 해당하는 내 GPS와 도슨트 정보를 해당 오브젝트의 GPS 위치에 생성
(Reference Image Library에 등록된 각각의 정보들은 arcoreimg.exe 프로그램을 통해 인식률 70%이상 확인된 이미지를 사용)  

[Basic Geospatial Demo]
- AR Core Extension의 Geospatial 기능을 사용하여, 실제 위치에 상호작용할 3D Object를 생성
- AR Geospatial Creator 기능을 사용하여 3D Object의 정확한 Localization 구현

[Geospatial Demo with Firebase Database]
- Basic Geospatial Demo Scene에 Firebase Realtime Database에 저장해 놓은 각 도슨트들의 GPS정보들을 불러온다.
- 불러온 GPS정보에 따라 Geospatial Crator Anchor를 가지고 있는 3D Object를 생성, 3D Object를 내 위치 기반으로 배치합니다.

---
<br>

## Unity 시작하기

### 1. 유니티 프로그램 설치 
1-1 Unity Hub 다운로드 및 설치
<br>
1-2  Unity 버전 선택
<br>
1-3 Unity 라이센스 확인
<br>
1-4 유니티 에디터 설치
<br>
### 2. 유니티 프로젝트 생성
2-1 새로운 프로젝트 생성
<br>
2-2 프로젝트 설정
<br>
2-3 프로젝트 이름 및 위치 지정
<br>
2-4 템플릿 선택
<br>
2-5 추가 설정 옵션 확인
<br>
### 3. 유니티 에디터 살펴보기
3-1 에디터 인터페이스 소개
<br>
3-2 씬 뷰 및 게임 뷰 이해
<br>
3-3 계층 구조 창 이해
<br>
3-4 프로젝트 창 탐색
<br>
3-5 인스펙터 창 이해
<br>
3-6 유니티 메뉴 및 단축키 소개
<br>
### 4. 비쥬얼 스튜디오 연동
4-1 Visual Studio의 버전 및 설치 요구 사항 확인
<br>
4-2 Visual Studio 설치 프로세스
<br>
### 5.씬 구성과 저장
5-1 다중 씬 관리
<br>
5-2 씬 설정 및 구성 요소 추가
<br>
5-3 씬 저장 및 로드

### 6. 오브젝트 배치하기
6-1 기본 게임 오브젝트 생성
<br>
6-2 오브젝트 위치, 회전, 스케일 조정
<br>
6-3 오브젝트의 속성 및 구성 요소 수정
<br>
6-4 다양한 유형의 오브젝트 배치 방법 소개 (3D 모델, 캐릭터, 라이트 등)
<br>
6-5 미리보기 및 플레이 모드에서의 오브젝트 배치 확인
<br>
### 7.에셋 관리
7-1 에셋의 종류 및 구성 요소 이해
<br>
7-2 에셋 스토어와 자산 다운로드
<br>
7-3 에셋 임포트 및 사용 방법
<br>
### 8. 기본 스크립팅
8-1 C# 스크립트 생성
<br>
8-2 스크립트 컴포넌트 연결
<br>
### 9.테스트와 디버깅
9-1 테스트를 위한 플레이 모드 사용
<br>
9-2 디버깅 기본 원리 이해
<br>
9-3 디버깅 도구 및 기능 소개
<br>
9-4 일반적인 버그와 오류 해결 방법
<br>




## AR내비게이션 시작하는 방법
### 1. ARCore Extension Package 설치
AR Foundation용 [ARCore Extension Package](https://developers.google.com/ar/develop/unity-arf/getting-started-extensions?hl=ko)는 Unity의 AR Foundation 패키지에 기능을 추가하여 앱에서 Cloud Anchors, 카메라 구성 필터, 녹화 및 재생과 같은 기능을 사용할 수 있습니다.

<br>

### 2. Google Cloud Platform API 사용 설정
[Google Cloud Platform](https://cloud.google.com/, "Google Cloud Platform")는 구글 클라우드 플랫폼은 구글 검색과 유튜브와 같은 최종 사용자 제품을 위해 내부적으로 구글이 사용하는, 동일한 지원 인프라스트럭처 위에서 호스팅을 제공하는 구글의 클라우드 컴퓨팅 서비스 입니다.
<details>
<summary>1. 프로젝트 등록</summary>
이미지
</details>
<details>
<summary>2. API 사용 설정</summary>
이미지
</details>
<details>
<summary>3. API Key 발급</summary>
이미지
</details>
<br>

### 3. Geospatial API 사용설정
Google의 [ARCore Geospatial API](https://developers.google.com/ar/develop/geospatial?hl=ko, "Google ARCore 
 Geospatial")는 Google 스트리트 뷰가 적용되는 지역의 VPS(Visual Positioning System) 기반의 현지화를 돕는 API입니다.

#### 3-1. Geospatial API사용 설정
> Project Settings -> XR Plug-in Management -> ARCore Extensions -> Enable Geospatial

#### 3-2. 사용 설정 및 API Key 사용 설명
Geospatial API를 사용하기 위해선 Google Cloud Platform에 프로젝트를 등록하고 API 사용설정을 하고, API Key를 발급받아야 합니다.

> Android Authentication Stratage -> API Key로 설정, Android API Key 입력

#### 3-3. Geospatial Creator API 사용 설정
ARCore 및 Google Maps Platform에서 제공하는 [Geospatial Creator](https://developers.google.com/ar/geospatialcreator/intro?hl=ko, "Geospatial Creator")를 사용하면 개발자와 크리에이터 모두가 Photorealistic 3D 카드를 통해 실제 위치에서 강력하고 매력적인 3D 디지털 콘텐츠를 시각화, 빌드, 실행할 수 있습니다.

>  Project Settings -> XR Plug-in Management -> ARCore Extensions -> Enable Geospatial Creator

#### 3-4. Cesium Pacakge 설치
3D 지리공간 플랫폼 [Cesium](https://cesium.com/, "Cesium")은 강력한 3D 지리 공간 응용 프로그램을 만들기 위한 기본 개방형 플랫폼입니다.

> Project Settings -> Package Manager -> Scoped Registries -> +버튼 클릭 후 내용 입력

<br>

#### 4. Android Build Settings
<details>
<summary>내용</summary>
이미지
</details>

#### 5. JsonDataManager 사용하기

#### 6. JasonData를 Unity에 불러오기

#### 7. UI /UX 배치하기

#### 8. POI Data 받아오고 띄우기

---
<br>

## AR 도슨트체험존 시작하기

#### 1. 오브젝트 인식할 Mesh 제작하기
#### 2. 특정위치에 오브젝트 불러오기
#### 3. 오브젝트 상호작용하기

<br>

---
<br>

## 해당 기능을 사용하여 개발
### ROI 변경 방법
<details>
<summary>내용</summary>
이미지
</details>

<br>

### Directions5 Json 구조
<details>
<summary>내용</summary>
이미지
</details>

<br>

### Static map API 링크

---
<br>
  
## 참고링크
[Maps Platform - Google for Developers] https://developers.google.com/maps?hl=ko
