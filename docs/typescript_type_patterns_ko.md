# TypeScript 타입 설계 패턴

목표: **읽기 쉬운 타입**

------------------------------------------------------------------------

## 1. Domain Types

핵심 데이터 정의

    type User = {
      id: number
      name: string
    }

------------------------------------------------------------------------

## 2. API 타입 분리

    ApiUserResponse
    User

------------------------------------------------------------------------

## 3. Utility Types

자주 사용

    Partial<T>
    Pick<T>
    Omit<T>
    Record<K,V>

------------------------------------------------------------------------

## 4. Discriminated Union

상태 관리에 유용

    type RequestState =
     | { type: "loading" }
     | { type: "success" }
     | { type: "error" }

------------------------------------------------------------------------

## 5. Feature 기반 타입

    features/todos/types.ts
