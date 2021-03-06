名词解释
^^^^^^^^^^^^^^^

基础链 （BaseChain, MotherChain）
----------------------
也称为母链，是使用工作量证明（POW）共识的一条公链，可以支持多条应用链。有多个Vnode节点组成。每个母链需要有一个chainId，需要在启动VNODE时作为输入参数，以便VNODE接入相应的母链。MOAC的主网chainId为99，测试网为101。

Vnode
----------------------
MOAC母链节点软件，用于构建母链（又称基础链）和连接应用链，可以进行POW挖矿，账本同步，交易以及应用链数据传输的节点。在启动VNODE时，需要指定接入区块链的编号chainId，默认值为主网99。

应用链 （AppChain，SubChain, MicroChain）
----------------------
也称为子链，是构建在MOAC基础链之上，用于独立运行一个或者多个智能合约的区块链。每个应用链有自己独立的应用链地址。

SCS
----------------------
MOAC应用链节点软件，用于应用链挖矿，应用链账本同步以及应用链业务逻辑执行的节点，也称为应用链矿工。目前MOAC有两种SCS，分别对应两种类型的应用链：ProcWind和FileStorm。

Chain3
----------------------
MOAC是在以太坊基础上开发的第三代区块链技术，相应的API接口和软件用Chain3来代指，比如:ref:`Chain3JS <chain3js0.1>`是基于JavaScript的MOAC软件库。

MOACMask
----------------------
类似于MetaMask，一个用于操作MOAC系统转账的浏览器插件。

应用链控制合约
----------------------
用于控制整个应用链的流程，文件名一般为DappBase.sol

监听节点（Monitor）
---------------------
监听节点是一个特殊的SCS节点，可以用来监听某条应用链的运行情况，当一个节点成为监听节点后，其只负责同步该应用链的区块信息，不参与应用链出块。Dapp用户可以通过该节点监控应用链运行情况



