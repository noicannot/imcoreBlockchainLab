# 《精通以太坊》
## 以太坊基础
#### 控制和责任
以太坊每个用户都控制自己的密钥，这些密钥可以控制对资金和合约的访问。丢失密钥就相当于丢失资金和合约。
保管这些密钥的方法：
* 选择密钥时：强化它，备份并不共享。如果你没有密码管理器，请将其写下并存放在锁定的抽屉或保险柜中。只要你拥有账户的“keystore”文件，就可以使用此密码。
* 当系统提示你备份或助记词时，请使用笔和纸进行物理备份。不要放到以后，会忘。这些在丢失了系统中保存的所有数据时使用。
* 不要在数字文档，数字照片，屏幕截图，在线驱动器，加密的PDF等中存储密钥材料（加密或不加密），不要临时凑合安全性。使用密码管理器或纸和笔。
* 在传输任何大量数据之前，先做一个小的测试交易（例如，1美元）。一旦你收到测试交易，请尝试从该钱包中发送。如果你忘记密码或因任何其他原因无法发送资金，最好是一个小损失。
* 请勿将金钱汇入任何公开私人密钥的地址，会立即有人拿走这笔钱。
#### 以太网货币单位
以太坊的货币单位称为以太ether，也被称为ETH或符号Ξ或♦。
例如，1个以太，或1个ETH，或Ξ1，或♦1
Tip Ξ使用Unicode字符926，♦使用9830。
以太被细分为更小的单位，最小的单位被命名为wei。一个ether是1* 10的18次方个wei。以太坊是制度，以太是货币。
以太的值总是在以太坊内部表示为wei，无符号整数值。当你处理1个以太网时，交易将编码1000000000000000000wei作为值。
以太的各种单位既有使用国际单位系统（SI）的科学名称，也有口语化的名字。
表Ether Denominations and Unit Names显示了各种单位，它们的俗名（通用）名称和他们的SI名称。为了与价值的内部表示保持一致，该表格显示了所有面值的wei（第一行），在第七行中ether显示为1* 10的18次方wei：

![img](https://github.com/noicannot/DigitalAssetsLab/blob/main/Blockchain/tanglu/Ethereum/EtherDenominationsAndUnitNames.jpg)

#### 选择一个以太坊钱包
以太坊钱包拥有你的密钥，并且可以代表你创建和广播交易。以太坊本身在不断变化，“最好”的钱包往往是适应它们的。
很容易更换钱包只需要将资金从旧钱包发送到新钱包，或者通过导出和导入私钥来移动密钥。
选择三种不同类型的钱包：移动钱包，桌面钱包和基于网络的钱包。选择他们只是为了示范和测试。
起始钱包：
**MetaMask**
MetaMask是一款浏览器扩展钱包，可在你的浏览器中运行。它易于使用且便于测试，因为它可以连接到各种以太坊节点和测试区块链。
**Jaxx**
Jaxx是一款多平台和多币种钱包，可在各种操作系统上运行，包括Android，iOS，Windows，Mac和Linux。设计简单易用，适合新用户。
**MyEtherWallet(MEW)**
MyEtherWallet是一款基于网络的钱包，可在任何浏览器中运行。它具有多个复杂的功能。
**Emerald Wallet**
Emerald钱包设计用于以太坊经典区块链，但与其他以太坊区块链兼容。它是一款开源桌面应用程序，适用于Windows，Mac和Linux。Emerald钱包可以运行一个完整的节点或连接到一个公共的远程节点，工作在“轻量”模式下。它还有一个配套工具来在命令行中执行所有操作。

**MetaMask**
设置密码后，MetaMask将生成一个钱包并向你显示一个_助记词备份_，由12个英文单词组成。如果MetaMask或你的计算机出现问题，可以在任何兼容的钱包中使用这些词来恢复对资金的访问。不需要密码进行恢复，这12个字就够了。
Tip 在纸上备份助记符（12个字），两次。将两张纸张备份存放在两个单独的安全位置，例如防火安全柜，锁定的抽屉或保险箱。将纸质备份视为你在Ethereum钱包中存储的相同价值的现金。任何能够访问这些文字的人都可以访问并窃取你的资金。
#### 切换网络
默认情况下，MetaMask将尝试连接到“主网络”。其他选择是公共测试网，你选择的任何以太坊节点或在你自己的计算机上运行私有区块链的节点（本地主机）：
**Main Ethereum Network**
主要的，公开的以太坊区块链。真正的ETH，真正的价值，真正的后果。
**Ropsten Test Network**
以太坊公开测试区块链和网络，使用工作证明共识（挖矿）。在这个网络上的ETH没有价值。Ropsten的问题在于攻击者铸造了数以万计的区块，产生巨大的重组并将燃气极限推到9B。
**Kovan Test Network**
以太坊公开测试区块链和网络，使用“Aura”协议进行权威证明（Proof-of-Authority）共识（联合签名）。在这个网络上的ETH没有价值。该测试网络仅由“Parity”支持。其他以太坊客户使用稍后提出的“Clique”协议作为权威证明。
**Rinkeby Test Network**
以太坊公开测试区块链和网络，使用“Clique”协议进行权威证明共识（联合签名）。在这个网络上的ETH没有价值。
**Localhost 8545**
连接到与浏览器在同一台计算机上运行的节点。该节点可以是任何公共区块链（主要或测试网络）或私人测试网络的一部分。
**Custom RPC**
允许你将MetaMask连接到任何具有geth兼容的远程过程调用（RPC）接口的节点。该节点可以是任何公共或私有区块链的一部分。

Tip 你的MetaMask钱包在连接的所有网络上使用相同的私钥和以太坊地址。但是，每个以太坊网络上的以太坊地址余额将有所不同。例如，你的密钥可以控制Ropsten上的以太和合约，但不能控制主网上的。

#### 获得一些测试以太
钱包充钱不再主网上做，因为真正的以太网需要花费金钱，处理它需要更多的经验。现在，我们将使用一些testnet ether加载我们的钱包。

有1个ETH，我们想要发送1个ETH，为什么MetaMask说我们没有足够的资金？
答案是因为gas的成本。以太坊交易需要支付矿工收取的费用，以验证交易。以太坊的费用以gas虚拟货币收取。作为交易的一部分，你使用ether支付gas。

Tip  测试网络也需要费用。如果没有费用，测试网络的行为将与主网络不同，从而使其成为不适当的测试平台。费用还可以保护测试网络免受拒绝服务攻击和构造不良的合约（如无限循环），就像保护主网络一样。


当你发送交易时，Metamask以3GWEI计算最近成功交易的平均gas价格。发送基本交易的gas成本为21000个gas单位。因此，你花费的ETH的最大数量为3*21000GWEI=63000GWEI=0.000063ETH。平均gas价格可能波动，因为它们主要由矿工决定。
表明：1ETH交易的成本是1.000063ETH。如果只有1个ETH。点击“Reject”取消此交易。

#### 世界计算机简介
事实上，加密货币功能是服务于以太坊作为世界计算机的功能；一个去中心化的智能合约平台。以太旨在用于支付运行的smart contracts，这是在称为Ethereum虚拟机（EVM）的模拟计算机上运行的计算机程序。

EVM是一个全球性的单例。以太坊网络上的每个节点运行EVM的本地副本以验证合约执行，而以太坊区块链记录此世界计算机在处理交易和智能合约时变化的状态。
#### 外部所有账户（EOAs）和合约
外部所有账户是那些拥有私人密钥的账户，它控制对资金或合约的访问。
合约账户由以太坊区块链记录，由EVM执行的软件程序的逻辑所拥有（和控制）。
两者重要的区别在于：人们通过EOA做出决定，而软件通过合约做出决定。
合约有一个地址接收和发送ether。
除了ether之外，交易还可以包含数据，用于指示合约中要运行的特定方法以及传递给该方法的参数。

#### 与合约交互
以太坊合约是控制货币的程序，运行在名为EVM的虚拟机内。由一个特殊的交易创建的，该交易提交它们的字节码以记录在区块链中。一旦他们在区块链上创建，他们就拥有一个以太坊地址，就像钱包一样。只要有人将交易发送到合约地址，它就会导致合约在EVM中运行，并将交易作为其输入。发送到合约地址的交易可能包含以太网或数据或两者都有。如果它们含有ether，则将其“存入”合约余额。如果它们包含数据，则数据可以在合约中指定一个命名函数并调用它，并将参数传递给该函数。