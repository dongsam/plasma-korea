# 요약

플라즈마는 스마트 컨트랙트의 인센티브 및 강제 실행을 위해 제안 된 프레임 워크로, 초당 상당한 양의 상태 업데이트 (잠재적으로 수십 억)까지 확장 가능하여 블록체인이 전 세계적으로 탈중앙화된 금융 애플리케이션으로 나타내는 것을 가능하게 한다. 이러한 스마트 컨트랙트는 거래의 상태 전환을 시행하기 위해서 네트워크 트랜잭션 수수료를 통해 자율적이고 지속적으로 운영되도록 인센티브를 제공하는데, 이 수수료는 궁극적으로 기초가 되는 블록체인(예: Ethereum)에 의존한다.

우리는 탈중앙화된 자율 애플리케이션을 확장하여 지불과 같은 금융활동을 처리할 뿐만 아니라, 중앙 집중화된 서버에 대한 대안으로 전 세계적으로 지속되는 데이터 서비스에 대한 경제적 인센티브를 구축하는 방법을 제안하고자 한다.

플라즈마의 설계는 두 가지 핵심 부분으로 구성되어 있다. : 모든 블록체인 계산을 MapReduce기능들로 재구성하는 것과 Nakamoto 컨센서스 인센티브가 block withholding을 막아준다는 것을 이해하여 기존 블록체인에 지분증명(Proof-of-Stake)토큰 결속시켜(bonding) 수행하는 선택적 방법이 있다.

이 구조는 부모 블록체인에서 상태 전환을 시행할 수 있는 위조증명을 사용하여 메인 블록체인의 스마트 컨트랙트를 작성함으로써 수행할 수 있다. 우리는 블록체인을 트리 구조로 구성하였으며, 각각을 분기된 블록체인으로 간주한다. 이 분기된 블록체인은 블록체인 히스토리와 Merkle 증명으로 커밋 된 MapReducible 계산으로 이루어져 있다. 원장(ledger entry)을 부모 체인에 의해 시행되는 자식 체인에 끼워 넣음으로써, 최소한의 신뢰로 굉장한 규모의 거래를 가능하게 할 수 있다.(루트 체인의 유효성과 정확성을 전제로 하였을 때).

비-글로벌 데이터를 글로벌하게 적용하는 과정에서 큰 어려움은 데이터 가용성과 block withholding attacks을 차단하는 것이다. 플라즈마는 결함이 있는 체인(faulty chain)을 나갈 수 있도록(exit) 하는 한편, 지속적으로 정확한 데이터 실행을 장려하고 강제하는 메커니즘을 구축함으로써 이 문제를 완화시켰다.

오직 결함이 없는 상태일 때만 merkleized된 약속(분기된 블록체인들)들은 주기적으로 루트체인(예: Ethereum)에 브로드캐스트 되며, 이는 확장성이 뛰어나고 비용이 저렴한 트랜잭션 및 계산을 가능하도록 한다. 플라즈마는 대량의 탈중앙화 응용 애플리케이션을 지속적으로 운용하는 것을 가능하게 한다.
