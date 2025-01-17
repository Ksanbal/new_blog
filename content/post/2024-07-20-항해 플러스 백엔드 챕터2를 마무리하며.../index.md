---
title: 항해 플러스 백엔드 챕터2를 마무리하며...
description: 
date: 2024-07-20
image: 
categories:
    - 회고
tags:
    - 항해플러스후기
    - 항해솔직후기
    - 항해플러스백엔드
weight: 1
---
항해 플러스 백엔드 코스를 등록하고 시작한지 5주차가 되었다. 10주 진짜 길다 생각했는데, 어느새 절반을 와버렸다. 체력적으로나 정신적으로나 힘들지 않았다고 얘기할 수는 없겠지만, 시간이 빠르게 지난만큼 즐거운 순간들이 있었다고 말할 수 있을 것 같다. 
챕터1은 TDD와 layered 아키텍처를 다뤘고, 챕터2에서는 서버 구축을 하면서 시나리오의 API를 구축하고 챕터1의 학습 내용들을 적용해나가는 시간이였다.

## 서버 구축을 시작하며 꼭 해내고 싶었던 목표
API 서버 개발은 항상 하던 일이라 사실 금방 할 수 있을거라 생각했다. 그동안 해오던 방식으로 작성했다면 일주일 안으로 충분히 했을거라 생각한다. 하지만 TDD와 Layered 아키텍처 모두 신경쓰지 않았던 것들이고, 그래서 더 어려움이 있을거라는 생각이 들었었다. 어찌보면 이전 챕터에서는 체험 이였다면, 이번 서버 구축에서 실제로 어떻게 적용하면 될지를 채화하는 과정이 될거라고 생각했었다.

## 서버 구축을 마무리하며 가장 기억에 남는 성취
아무래도 Layered 아키텍처를 적용하는 방법을 내 방식대로 이해했을 때인 것 같다. 직접 파일의 구조를 나누고 각 레이어에서의 역활이 잡히고 나니까 개발 속도가 붙었던 것 같다.

```ts
1-presentation // request, response 전달 또는 가장 앞단의 로직을 수행
	/controller
	/scheduler
2-application // 여러 서비스를 묶어 큰 개념의 비즈니스 로직을 수행
	/facade
3-domain // 각 도메인에서 수행할 지역적인 비즈니스 로직을 수행
	/service 
4-infrastructure // DB나 외부 API 같은 datasource를 관리하고 요청
	/repository 
	/entity
```

## 서버 구축에서 반드시 이뤘으면 했는데 이루지 못한 것
디테일들을 많이 놓친게 가장 아쉬운 것 같다. 과제 제출에 쫓겨 Test code 작성없이 넘어간 부분도 많았고, 예외처리나 로깅도 더 신경 쓸 수 있었는데...아무래도 과제를 진행하면서 학습하게되는 부분이 있어서 첫 시작때 코드와 끝의 코드의 퀄리티가 달랐던 것 같다. 이후에 리팩토링을 통해서 완성시켜 나가는 시간을 가지고 싶다.

## 다음 챕터에서 반드시 성공하고 싶은 목표
다음 챕터는 동시성 문제를 해결하기 위해 서버 개발단에서 뿐 아니라 Redis나 Kafka 같은 인프라적인 서비스를 이용한 과정이다. 단순히 이렇게 쓰는게 좋다고 카더라...말고 내가 직접 검증해나가면서 상황에 **적절한** 선택지를 가져가는게 목표다. 항상 코치님들이 이야기 하시는게 오버엔지니어링을 피하는 것 이다. 뭐든지 다 떄려넣으면 좋겠지 당연히. 하지만 우리는 비용의 문제를 벗어날 수 없고, 오히려 복잡성만 증가할 수 있다. 적절한 수준을 찾아가는 능력을 키우자.

## 내가 강화해야 할 강점 중 가장 중요하다고 생각하는 한 가지
꼼꼼함과 적절한 휴식이 필요한 것 같다. 복잡한 문제를 해결하다보면 간단한 주석이나 예외처리 같은 놓치고 가는 부분이 많고, 점점 뇌 용량이 차오르는 느낌이 들때가 있다. 적절한 휴식을 통해서 머리를 비우고 문제를 한발 뒤에서 보면서 부족함 없이 가는 것. 그런게 필요한 것 같다.

## 내가 개선해야 할 개선점 중 가장 중요하다고 생각하는 한 가지
늘어지거나 미루는 습관을 개선하고 싶다. 미루는 습관은 가장 빠르게 고쳐야하는 습관 중에 하나라고 생각한다. 사람은 답하기 어려운 너무 큰 고민들을 할 때 뒤로 미룬다고 하던데, 작은 고민들로 쪼개고 하나씩 해결해나가는 방향으로 바꾼다면, 점차 좋아질 수 있을거라 생각한다.

