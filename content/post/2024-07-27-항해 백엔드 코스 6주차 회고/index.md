---
title: 항해 백엔드 코스 6주차 회고
description: 
date: 2024-07-27
image: 
categories:
    - WIL
tags:
    - 항해99
    - 항해플러스
    - WIL
weight: 1
---
### 1. 문제 **(과제, 프로젝트를 진행하면서 부딪혔던 기술적인 문제)**
>이번 주차를 지나며 겪었던 문제가 무엇이었나요?

- 낙관적 락을 구현하는 것이 조금 어려웠다. 개념상으로는 이해했는데, 코드에서 예상한 대로 실행되지 않아서 삽집을 좀 했던 것 같다.
- Reids를 이용한 Pub/Sub 형태의 lock 구현이 큰 개념은 이해를 했는데, 상세한 구현이 어려웠다.

### **2. 시도**
>문제를 해결하기 위해 어떤 시도를 하셨나요?

- Version Column을 추가하고 Version을 직접 올리기도 하고, 여러 글을 찾아보면서 시도했던 것 같다.
- Pub/Sub 방식에 대한 개념을 찾아보고, 다른 조원분들이 구현한 코드를 참고했다.

### **3. 해결**
>문제를 어떻게 해결하셨나요?

- 포기...했다ㅎㅎ 생각해보니까 낙관락 잘 안쓸 것 같아서?! 하지만 아니였다.
- Redlock 라이브러리를 만나서 온전한 믿음으로 갔다...ㅎㅎ 나중에 Redlock의 명확한 로직을 찾아보면 좋을 것 같다.

### **4. 알게된 것**
>문제를 해결하기 위해 시도하며 새롭게 알게된 것은 무엇인가요? 

- 낙관락과 비관락을 섞어서 사용하는걸 기대했다는 피드백이 있었다. 하나의 API에서 여러개의 lock을 사용할 생각은 못했던 부분이라 충격적이였다.
---

### **Keep : 현재 만족하고 계속 유지할 부분**
>이번 주를 마무리 하며 나에게 만족했던 부분은 무엇인가요?

음...이번주는 사실 마음에 드는게 없었던 것 같다. 피로 관리를 잘 하자...

### **Problem : 개선이 필요하다고 생각하는 문제점**
>이번 주를 마무리 하며 개선이 필요하다고 생각했던 문제점은 무엇인가요?

과제가 쉽다고 생각하고 느슨해진 것. 미루는 습관은 진짜 빨리 고쳐졌으면 좋겠다.

### **Try : 문제점을 해결하기 위해 시도해야 할 것**
>이 문제점을 해결하기 위해 다음 한 주간 시도 할 것은 무엇인가요? 

안일한 생각 금지. 월요일부터 빠르게 적용하고, 시간이 오히려 남게 과제를 진행해보자.