# JS

### 🟡 이벤트
### 1. 이벤트 버블링과 캡처링에 대해 설명해주세요.
e.current.target 에 등록된 이벤트가 e.target으로 인해 발생되면 동적으로 이때 생성된 이벤트 객체가 window 객체에서 target까지 dom트리 상위요소에서 하위요소 방향으로 전파되는 것을 이벤트 캡쳐링이라 한다.
e.target에 도달한 이벤트 객체가 다시 window 객체 까지 하위요소-상위요소 방향으로 전파되는 것을 이벤트 버블링이라 한다.
(capturing phase, target phase, bubbling phase)

### 2. 이벤트 위임에 대해 설명해주세요. 
하위 dom 요소에 이벤트를 각각 등록해주는 방법 말고 하나의 상위 dom 요소에 이벤트 핸들러를 등록해 이벤트를 캐치하도록 하는 방식.

### 3. 이벤트 위임의 동작 방식에 대해 설명해주세요.
dom 트리 구조 상의 상위요소와 하위요소가 있다고 가정을 한다면, 하위요소에서 클릭이벤트가 발생하면 동적으로 생성된 이벤트 객체가 window 객체에서 target까지 하위방향으로 내려옵니다. 이 이벤트 객체는 target에 도달한 후 다시 window객체로 
돌아가는데 버블링되는 때에 상위요소에서 이벤트를 캐치해 이벤트리스너에 등록된 동작을 수행합니다. 
(이벤트 등록 방식은 어트리뷰트/프로퍼티 등록 방식과 addEventListener 등록 방식이 있는데 어트리뷰트/프로퍼티 등록방식은 이벤트를 target phase, bubbling phase에서만 이벤트를 캐치할수 있지만 addEventListener메서드 등록방식은 세번째 인수로 false나 값을 생략한다면 target phase, bubbling phase에서만 캐치가 가능하고 세번째 인수로 true를 준다면 capturing phase에서도 이벤트를 캐치할 수 있습니다!)

### 🟡 AJAX 
### 4. AJAX에 대해 설명해주세요. 
