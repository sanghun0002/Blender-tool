# Blender-tool
Blender Tool 사용법
# Blender 차량 모델링 & CARLA 적용 가이드 (README)

## 개요

본 문서는 Blender를 활용하여 차량을 모델링하고, 해당 모델을 CARLA 시뮬레이터에 적용하는 전체 과정을 설명합니다.

---

## Blender 설치

Ubuntu 환경에서 Blender를 설치합니다.

```bash
sudo apt install blender
```

설치 완료 후 Blender를 실행합니다.

---

## Blender 실행 화면

Blender 실행 시 기본 작업 화면이 나타납니다.
해당 화면에서 3D 모델링 작업을 시작할 수 있습니다.

---

## 기본 모델링 작업

### 3.1 도형 추가

* 좌측 상단의 **Add 메뉴**를 클릭하여 다양한 기본 도형을 추가할 수 있습니다.
* 도형 추가 후 우측 하단의 **속성 창(Properties)**에서 다음을 조정할 수 있습니다:

  * 크기 (Scale)
  * 위치 (Location)
  * 회전 (Rotation)

---

### 3.2 도형 변형 (Edit Mode)

* 좌측 상단에서 **Object Mode → Edit Mode**로 전환합니다.
* Edit Mode에서는 다음 요소를 직접 수정할 수 있습니다:

  * Vertex (점)
  * Edge (모서리)
  * Face (면)

#### ✔ 사다리꼴 / 비정형 도형 만들기

1. Edit Mode 진입
2. 특정 Vertex 또는 Edge 선택
3. 이동(G), 크기(S), 회전(R) 기능 활용
4. 원하는 형태로 변형

---

## 차량 모델링 진행

위 기능들을 활용하여 원하는 차량 모델을 제작합니다.

### ✔ 예시 작업

* 차체 구성
* 바퀴 생성
* 디테일 요소 추가 (창문, 라이트 등)

---

## CARLA용 Skeleton(뼈대) 적용

차량 모델링 완료 후, CARLA에서 제공하는 뼈대(Skeleton) 파일을 불러옵니다.

### 작업 절차

1. Skeleton 파일 import
2. 차량 모델과 정렬
3. 바퀴 및 차체 위치 맞춤

### 🔧 정렬 팁

* `SHIFT + S` 단축키 사용:

  * 오브젝트 중심 정렬
  * 커서 기준 이동

➡ 정밀한 위치 맞춤 작업에 매우 유용

---

## FBX 파일로 내보내기

모델링 및 Skeleton 세팅 완료 후, FBX 형식으로 저장합니다.

### Export 방법

1. 상단 메뉴 → `File`
2. `Export`
3. `FBX (.fbx)` 선택
4. 저장

---

## CARLA에서 적용

1. 생성한 `.fbx` 파일을 CARLA 프로젝트에 추가
2. 빌드 진행
3. 물리 엔진 및 차량 동작 설정

---

## 전체 작업 흐름 요약

```
Blender 설치
   ↓
기본 도형 생성 및 편집
   ↓
차량 모델링
   ↓
CARLA Skeleton 적용
   ↓
FBX 파일 export
   ↓
CARLA에서 import 및 물리 설정
```

---

## 참고

* 정밀한 모델링을 위해 단축키 활용 필수
* Skeleton 정렬이 차량 물리 동작에 큰 영향을 미침
* FBX export 시 스케일 및 축 방향 확인 필요

---

