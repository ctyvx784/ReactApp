# Redux를 이용한 React APP 예제

1. Redux란?
	-Redux는 JavaScript 어플리케이션에서 data-state 와 UI-state 를 관리해주는 도구입니다.
	-store에서 모든 데이터를 담고 있고, 컴포넌트끼리는 직접 교류하지 않고 store 중간자를 통하여 교류합니다. 
  	dispatch는 store에 있는 데이터를 업데이트 하는것을 가르키고, subscribe는 해당 컴포넌트에서 store에 있는 
  	특정 데이터의 변동을 주의하고있다가 변동이 있을시 바로 반영시키는것을 가르킵니다.

2. Redux의 3가지 원칙

  	2.1 Single Source of Truth
   -Redux는 어플리케이션의 state를 위해 단 한개의 store 를 사용합니다. 
   	 모든 state 가 한곳에 있기 떄문에 이를 Single Source of Truth 라고 부릅니다.
    
  2.2 State is read-only
    -어플리케이션에서 state를 직접 변경 할 수는 없다는 의미입니다.
    state 를 변경하기 위해서는, action 이 dispatch 되어야 합니다.
    action 은, 어떤 변화가 일어나야 할 지 알려주는 객체입니다.
    
  2.3 Changes are made with Pure Functions 
    -두번째 원칙에 설명된것처럼 Redux 에선 어플리케이션에서 state 를 직접 변경하는것을 허용하지 않습니다.
    그 대신에 action 을 dispatch 하여 상태값을 변경 과정에서 받아온 action 객체를 처리하는 함수를 Reducer 라고 부릅니다.
    action은 어떤 변화를 일어나야 할 지 알려주는 객체라면, Reducer 는 그 정보를 받고 애플리케이션의 상태를 어떻게 바꿀지 정의한다고 볼 수 있습니다.
    
    -Reducer 함수의 원칙-
    외부 네트워크 혹은 데이터베이스에 접근하지 않아야한다.
    return 값은 오직 parameter 값에만 의존되어야한다.
    인수는 변경되지 않아야한다.
    같은 인수로 실행된 함수는 언제나 같은 결과를 반환해야한다.
    순수하지 않은 API 호출을 하지 말아야 한다. (Date 및 Math 의 함수 등)
출처: https://velopert.com/1225
