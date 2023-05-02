# FAQ

<figure><img src="../../../.gitbook/assets/image (1) (3).png" alt=""><figcaption></figcaption></figure>

### 在其他区块链上的 PancakeSwap ，我可以做什么？

&#x20;一如既往地提供流动性，交易和使用农场。如果您已经是多链用户，请记得在我们部署的其他区块链（如以太坊）上为 PancakeSwap 提供流动性，我们会在 BNB 智能链上为您提供 CAKE 奖励，让您无需将这些资产跨链即可赚取更多 CAKE！&#x20;

### 后续会上线更多农场对吗？&#x20;

是的，但我们将逐步部署，以确保我们优先考虑用户资金的安全和 CAKE 的通胀。请在聊天社区中告诉我们您认为应该在其他区块链上添加 PancakeSwap 的哪些内容，以及我们应该在哪些其他区块链上部署 PancakeSwap。&#x20;

### 为什么质押 LP 代币的 gas 费用很高？&#x20;

首次设置需要少量原生代币（例如，以太坊上的 ETH）。所以第一笔质押操作 gas 会稍微贵一些。&#x20;

此外，跨链农场还涉及其他费用（主要是 gas 费用）。查看[此部分](faq.md#kua-lian-nong-chang-zhi-ya-xu-yao-shou-fei-ma)以了解更多信息。

### 为什么质押和解除质押需要 30 分钟才能完成？&#x20;

所有跨链操作大约需要 30 分钟才能完成。这是因为：&#x20;

* 链上操作必须在两个链上（农场所在区块链（如以太坊）和 BNB 链）执行。&#x20;
* 传递跨链消息需要时间。&#x20;
* 为确保安全，所有数据在不同区块链之间保持同步和一致。

### 我收割的 CAKE 奖励在哪里？&#x20;

您收割的 CAKE 将分发到 BNB 智能链上。 请切换钱包中的区块链网络查看 CAKE 的余额。

### 我使用的钱包不支持切换区块链，那我该如何收割奖励？

请尝试使用其他支持多链和可以切换区块链的钱包应用程序。&#x20;

请注意，质押和解除质押 LP 代币同时，也会将所有赚取的 CAKE 收割到您在 BNB 智能链上的钱包中。 因此，如果您不想使用其他钱包应用程序，您可以只需质押更多、或取出少量 LP 代币，即可收割您赚取的 CAKE。

### 跨链农场质押费用说明

&#x20;与 BNB 链上的原生农场不同，在其他区块链上的农场耕种涉及到跨链，以下是费用列表：

**1 - 创建代理合约的 Gas 费**&#x20;

首次质押须在 BNB 链上创建一个代理合约以进行跨链农场质押。创建代理合约的 gas 费用包含在此次链上操作中。

该费用仅存在第一次 “质押” 时。&#x20;

**2 - 在 BNB 链上调用的 Gas 费**&#x20;

发生于当用户存入或提取 LP 代币时。执行者将根据 BNB 链上用户的行为提交链上操作，调用的 gas 费用包含在此次链上操作中。&#x20;

该费用在每笔存款或取款操作时产生。&#x20;

**3 - 在其他区块链上调用的 Gas 费**&#x20;

当用户提取 LP 代币时。执行者提交质押结束讯息上链，跨链释放其他区块链上的 LP 代币 （例如以太坊）。这些操作的 gas 费用包含在此次链上操作中。&#x20;

此费用仅在提取代币时收取。&#x20;

**4 - 跨链讯息费**&#x20;

我们使用 Celer 提供的跨链讯息传递服务来传递跨链消息，因此产生跨链讯息费。根据讯息的字节（byte）长度计费。

每次 “质押” 均会产生此费用。在 “解除质押” 时，此费用双倍收取，出于安全考量，讯息需要在 BNB 链和其他区块链之间进行来回传递，来回各一次，因此会收取两次费用。

```
messagingFee = feeBase + message.length * feePerByte;
```

您可以在跨链讯息传递智能合约内的公式中找到如下变量：

* 以太坊：0x4066d196a423b2b3b8b054f4f40efb47a74e200c&#x20;
* BNB链：0x95714818fdd7a5454f73da9c777b3ee6ebaea6b

**5 - 启动基金**&#x20;

这不是严格意义上的 “费用”。

对于每一个刚开始参与 PancakeSwap 跨链农场的新用户。在第一次 “质押” 操作中，我们会将 0.005 BNB 存入他们的 BNB 链钱包。同时农场所在链上相应数量的原生代币（如以太坊上的 ETH）将使用价格预言机提供的市场汇率，从质押链上操作的 gas 中收取。&#x20;

这是为了帮助用户轻松开始他们的 BNB 链之旅。我们非常理解拥有收获的 CAKE 奖励，却不找到另一种方式来获取 BNB，以至于无法探索生动丰富的 PancakeSwap 生态系统的痛苦。&#x20;

该费用仅在链上操作第一次 “质押” 时收取一次。&#x20;

### CAKE 产出从哪里来？&#x20;

更新于 2022 年 10 月 10 日&#x20;

目前，大厨们已将 CAKE 糖浆池每个区块产出中的 0.0189 CAKE 转移到所有跨链农场。&#x20;

以下是产出明细：

|               | 农场倍数 | CAKE 每个区块产出 |
| ------------- | ---- | ----------- |
| **CAKE 糖浆池**  | -    | **8.9811**  |
| **所有跨链农场**    | -    | **0.0189**  |
| 以太链  ETH/USDC | 0.5x | 0.0105      |
| 以太链  ETH/USDT | 0.2x | 0.0042      |
| 以太链 WBTC/ETH  | 0.2x | 0.0042      |

### 在存款、收割和取款过程中会发生什么？

要形容的话，在 PancakeSwap 跨链农场进行流动性耕种，就像使用 ”替身“ LP 代币在 BNB 链上耕种，也使用同样的 MasterChef 合约。CAKE 奖励在 BNB 链上计算、分发，并由 MasterChef 合约进行统筹控制和保障。

**存款时：**&#x20;

1. 用户需将 LP 代币存入目标区块链上的农场（如以太坊）。
2. LP 代币被转移到农场金库合约中。&#x20;
3. Celer 讯息传递服务将 “存入” 链上讯息传递到至BNB链。&#x20;
4. BNB 链上的执行者铸造与 “替身” 相同数量的对应农场 LP 代币，然后将它们存入农场。&#x20;

**收割时：**

由于 CAKE 奖励在 BNB 链上计算和分发的，用户无需跨链操作即可通过单笔 BNB 链上操作领取 CAKE 奖励。&#x20;

**取款时：**&#x20;

1. 用户要求在农场所在区块链（如以太坊）上提取 LP 代币。&#x20;
2. Celer 讯息传递服务将 “取款” 消息传递到 BNB 链。&#x20;
3. BNB 链上的执行者从农场中提取并销毁这些农场 LP 代币，并将获得的 CAKE 奖励转移给用户，并利用 Celer 讯息传递服务将确认讯息传递回原始农场所在区块链。&#x20;
4. 对应农场所在区块链上的执行者确认一切，然后从金库合约中释放 LP 代币。