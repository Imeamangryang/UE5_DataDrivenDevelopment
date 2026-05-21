
# 구현 최종 목표

- Unreal Engine에서 데이터 주도 개발을 활용하여 게임 시스템을 구현하는 방법을 학습한다.
- 각 챕터마다 독립적으로 읽고 사용해도 문제가 없는 구성으로 작성한다.
- 각 챕터마다 실습 예제와 함께 설명하여 실제로 어떻게 적용할 수 있는지 보여준다.


# Chapter 1

- 들어가는 말
- 대상 독자
- 책의 구성
- 개발 환경

# Chapter 2

## 2-1 Data-Driven Development In Game

- 게임에서의 데이터 주도 개발

## 2-2 Why Data-Driven Development?

- 데이터 주도 개발
- 데이터와 로직의 분리

# Chapter 3

## 3-1 UObject and Reflection System

- UObject와 Reflection 시스템
- UCLASS, UPROPERTY, UFUNCTION
- UHT와 generated.h 파일
- 런타임에서의 객체 정보 접근
- Blueprint와의 통합

## 3-2 Unreal Engine World

- Unreal Engine의 World 시스템
- 레벨과 월드의 개념
- 월드에서의 객체 관리
- Actor와 Component 시스템

## 3-3 GameplayFramework

- GameplayFramework 소개
- Gamemode과 GameState
- PlayerController와 PlayerState
- Pawn과 Character

# [Chapter 4](InputSystemPlan)

목표
- Enhanced Input System의 소개
- Input Action과 Input Mapping Context
  - Data Asset으로의 설계
- Context Switching
- Runtime Input Binding과 Unbinding (키 변경 UI도 구현)
- Input Recoding 시스템

## 4-1 Enhanced Input System
- Enhanced Input System 소개
- Input Action
- Input Mapping Context
- Enhanced Input Subsystem

## 4-2 Input Action 기반 입력 구현
- EnhancedInputComponent 설계
- Input Binding 후 Printf로 입력 확인
- Input Trigger와 Modifier 활용

## 4-3 Context Switching

- 상황별 Input Mapping Context 전환

## 4-4 Runtime Input Binding
- 런타임 입력 변경 구조
- 키 변경 UI 구현
- SaveGame을 활용한 입력 설정 저장

## 4-5 Input Recording System
- 입력 기록 시스템 설계


# Chapter 5

목표
- Data Table 구성하기
  - 실제 에셋이 들어있는 Table : Key는 ID, Value는 에셋으로 구성
  - 최종적으로 처음 로드하는 테이블은 Int형의 ID들로 구성된 테이블이 되고, 이 테이블을 통해 실제 에셋이 들어있는 테이블을 참조하는 구조로 설계
- 이를 통해 캐릭터 스켈레탈 메시에 대한 Data Table을 구성하여, 캐릭터를 스폰할 때 Data Table을 참조하여 스켈레탈 메시를 로드하는 구조로 설계