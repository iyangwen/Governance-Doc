# 基本概念


## 区块链常用术语


- **外部账户(Externally account)**，私钥控制，没有代码关联，可发起交易。外部账户的地址是由私钥所生成的。
- **合约账户(Contract account)**，又称为用户账户(User Account)。合约部署生成，与代码关联，不可发起交易只能被外部账户调用。合约账户的地址是在创建合约是确定的（一般通过计算合约创建者的地址和该地址发出过的交易数量得到）。


![](img/acct-contract-acct.png)


## 账户治理组件所引入的术语


- **区块链业务应用（Blockchain Business Application）**，基于区块链技术，实现和满足特定业务领域的需求。在一个区块链业务应用中，一般会依赖智能合约技术，其执行结果记录在分布式账本中。在一个区块链网络中，可以发布多个区块链业务应用。而在一个区块链业务应用中，最多只能定义一个治理账户。

![](./img/application.png)

- **治理账户(Governance Account)**，区块链业务应用治理主体的管理账户。该账户本身为合约账户，其账户关联了合约治理相关的代码，绑定了一个或一组外部账户。只有被绑定的外部账户才能操作此治理账户。此外，只有状态正常的普通账户才能被设置为治理账户。一个治理账户可以管理一个区块链业务应用，也可以管理多个区块链业务应用。
- **普通账户（Normal Account）**，区块链业务应用治理的对象。该账户本身为合约账户，该账户与一个外部账户一一映射并被绑定，关联了状态、配置和操作的代码。只有治理账户和被绑定的外部账户才能操作此治理账户。
- **账户治理者（Account Governance Administer）**，在一个区块链业务应用中，区块链账户治理者负责直接管理和操作治理账户，即所谓的『区块链业务应用管理员』。根据是否是由单一机构管理，又可以划分为带有传统中心化管理特征的超级管理员和去中心化多机构协作的账户治理委员会两类。治理者行使账户的管理职能，支持对普通账户重置私钥、冻结、解冻、销户等操作。
- **治理模式（Governance Mode）**，账户治理者所采用的账户治理的方式，主要有两种，分别为超级管理员模式和治理委员会模式（又被称为投票模式）。其中，投票模式又可以根据投票者权重是否相等，进一步细分为多签投票制（Multi-Vote Mode）和权重投票制（Weighted-Vote Mode）。
- **超级管理员（Super Administer）**，在一个区块链业务应用中，可以指定超级管理员治理模式；在该模式下，治理账户由一个唯一的治理者来控制。
- **账户治理委员会（Account Governance Committee）**，在一个区块链业务应用中，通常是参与区块链业务应用的业务多方共同选出的一个委员会，共同参与账户治理。委员会成员拥有对账户治理事务的投票权，通过投票的方式，来决策和管理相关操作。
- **社交好友重置机制（Social Friends Reset Mechanism）**，是指用户为普通账户设置一组关联的其他普通账户的地址，这些普通账户一般是用户的社交好友们的普通账户。一旦用户需要重置私钥，可通过联系好友发起重置申请，经过多个社交好友同意后，可重置用户普通账户所绑定的私钥。