# Solidity_examples
솔리디티 예제

### Data Type
1. string / byte
스트링 보다 바이트가 가스비가 더 적게 든다.

### 솔리디티 저장공간
solidity 는 storage, memory, calldata ,stack  이렇게 4개의 저장 영역으로  나뉘어 있다.
 
storage : 대부분의 변수, 함수들이 저장되며, 영속적으로 저장이되어 가스 비용이 비싸답니다.
 
memory: 함수의 파라미터, 리턴값, 레퍼런스 타입이 주로 저장이 됩니다.
그러나, storage 처럼 영속적이지 않고, 함수내에서만 유효하기에 storage보다 가스 비용이 싸답니다.
 
Colldata : 주로 external function 의 파라메터에서 사용 됩니다.
 
stack:  EVM (Ethereum Virtual Machine) 에서 stack data를 관리할때 쓰는 영역인데 1024Mb 제한적입니다.

string을 쓰기위해서는 memory 일식적으로 저장하는 키워드를 써야한답니다. 

### Override
상속을 받은 후에 오버라이딩을 한다면, 쉽게 생각하면 백지가 된 상태라고 받아들이면 된다.
그래서, 오버라이딩 후에 다시 어떠한 것을 적어주는 작업을 해야하는데,
부모 컨트랙트의 내용을 가져오고 싶은 데 그 코드의 길이가 짧다면, 내가 직접 적어주면 되지만,
코드가 많거나 할 경우에 super()를 적어주면, 그대로 복붙이 된다.
