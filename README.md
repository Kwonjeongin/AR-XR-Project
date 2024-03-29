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
1. Unity 이해
2. C# 프로그래밍입문
3. AR 내비게이션
4. AR 도슨트 체험존
---
## 기능상세 소개

### AR?
실제 세계를 증강하는것 => 현실세계에 가상의 오브젝트 결합

### 1. AR 내비게이션 
Google API 기반 Navigation  실시간 AR화살표로 경로를 표시하여, 사용자가 목적까지 쉽게 도착할 수 있도록 도움을 줌.
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

## Unity 이해

### 1. Unity 프로그램 설치 
1-1 Unity Hub 다운로드 및 설치
<br>
1-2  Unity 버전 선택
<br>
1-3 Unity 라이센스 확인
<br>
1-4 유니티 에디터 설치
<br>
1-5 유니티 프로젝트 생성

### 2. Unity UI 살펴보기
각 탭으로 분리된 윈도우를 뷰라고 한다.
뷰의 명칭은 탭에 표기 되어 있으며, 이 탭을 드래그 앤드 드롭해 자유롭게 배치할 수 있다. 

2-1 프로젝트 뷰 
- Project Browser 또는 Project Panel 이라고도 한다.
- 게임 콘텐츠에 필요한 모든 리소스(유니티에서 생성한 에셋)를 모아두는곳

2-2 씬뷰
- 씬뷰(Secen)는 무한 3차원 공간을 표현하고 스테이지를 디자인하고 플레이어를 배치해 게임을 설계하는 뷰
- 씬뷰의 헤더에 있는 바를 컨트롤 바 라고도 한다.

2-3 하이러키 뷰
- 하이러키 뷰 (Hierarchy View)는 씬뷰에 배치한 모든 객체를 계층 구조로 나열해서 보여준다.

2-4 인스펙터 뷰 
- 인스펙터뷰(Inspector View)는 씬뷰 또는 하이러키 뷰에 선택된 게임오브젝트의 속성을 보여주는 뷰로써, 해당속성을 조회하거나 수정할 때 사용한다. 같은 속성에 한해 동시에 여러개의 게임오브젝트를 선택하고 인스펙터 뷰에서 수정할 수 있다.

2-5 게임뷰
- 게임 뷰(Game View)는 개발중에 게임을 실행해 미리 볼 수 있는 뷰로서, 씬뷰에 있는 메인카메라의 시야로 렌더링해서 보여준다. 해당 프로젝트를 빌드해서 실행하거나 모바일에서 구동할때 보이는 화면과 동일하다. 또한 게임뷰에 있는 컨트롤 바의 해상도를 선택하면 다양한 해상도로 볼 수 있다.

2-6 콘솔뷰
- 콘솔뷰(Console View)는 디버깅시 로그를 출력하는 뷰로서, 출력하는 메세지는 정보(Information), 경고(Warning), 오류(Error) 로 분류해 메세지 타입별로 필터링해 출력할 수 있다.

### 3. 유니티 기초 조작법
3-1 단축키

## C# 프로그래밍 입문
### 1. 데이터 형식
### 2. 변수
### 3. 연산자
### 4. 조건문, 반복문
### 5. 함수

<br>

## ARNavigation 시작하는 방법
> 목표 : ARNavigation을 이용해 원하는 장소의 위치 까지 최적 이동 경로를 계산합니다.
### 0. AR Foundation
Unity로 AR 콘텐츠를 개발을 하기 위해서는 AR Foundation을 이용한 환경셋팅을 해주어야 합니다.
유니티는 크로스 플랫폼을 지원하는 AR 플랫폼을 만들기 위해 AR Foundation 프레임워크를 제공합니다.
![2024-03-17 20 30 13](https://github.com/Kwonjeongin/AR-XR-Project/assets/139726011/49a0c6df-e6f8-43ba-930d-5ae09584b1df)


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
Android 빌드 설정을 사용하여 Android 기기용 애플리케이션을 설정하고 빌드합니다.
[Unity Android Build Setting]("https://docs.unity3d.com/kr/2021.3/Manual/android-build-settings.html")
1. File > Build Settings를 선택합니다.
2. Platform 창의 플랫폼 리스트에서 Android를 선택합니다.
   참고: Android가 회색으로 비활성화된 경우 Android 환경 설정의 단계를 따르십시오.
4. Build 버튼이 표시되지 않고 Build And Run이 회색으로 비활성화된 경우 Switch Platform을 선택합니다. 

<details>
<summary>Build Settings</summary>
 
</details>

![android-build-settings](https://github.com/Kwonjeongin/AR-XR-Project/assets/139726011/9040ee4e-634c-42d1-870c-46f530f38598)

#### 5. JsonDataManager
JSON 이란?
JSON은 JavaScript Object Notation의 약자로, 데이터를 저장하거나 전송할 때 사용되는 텍스트 기반의 경량 데이터 교환 형식이다. 
JSON은 속성-값 쌍(attribute-value pairs)이나 배열과 같은 데이터 구조를 표현하기 위해 설계되었으며, 사람이 읽을 수 있고 기계가 parsing(분석)하고 생성하기 쉬운 형태로 되어있다.

#### 6. JSON Utility
UnityEngine.JsonUtility 클래스를 통해 JSON 데이터를 쉽게 읽고 쓸 수 있는 기능을 제공한다. 
이 클래스는 직렬화(Serialize)와 비직렬화(Deserialize) 함수를 통해서 Unity 객체를 JSON 형식으로 변환하거나, 반대로 JSON 형식의 데이터를 Unity 객체로 변환한다.

#### 7. UI /UX 
> 예시 이미지 Google Live Map
![20240319_150959](https://github.com/Kwonjeongin/AR-XR-Project/assets/139726011/131b7623-2053-437f-8414-b96f5d1a7384)

#### 8. POI Data 

---
<br>

## AR 도슨트체험존 시작하기
> 목표 : 특정 장소를 돌아다니면서 다양한 AR 펫 들을 만날 수 있습니다. 이 펫들은 터치를 통합 간단한 상호작용이 가능합니다.

#### 1. 바닥 인식할 Mesh 제작하기
#### 2. Mesh의 특정위치에 AR펫 불러오기
#### 3. AR펫과 상호작용 구현하기

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
