# 跨链 FAQ

<figure><img src="../../.gitbook/assets/image (201).png" alt=""><figcaption></figcaption></figure>

#### 我可以使用移动端钱包来进行 CAKE 的跨链吗？我可以使用 MetaMask 以外的钱包吗？

截止写此篇文章时，CAKE 的跨链只支持 Coinbase，MetaMask（以及任何与 MetaMask 兼容的钱包）。之后将会支持更多的钱包。

为了尽量避免在你的设备之间复制和粘贴私钥或助记词带来的潜在风险。我们建议在桌面钱包扩展程序上创建一组新的钱包作为跨链使用。



#### 提交跨链交易时出错

请尝试手动输入金额，不要点击 "MAX" 按钮。&#x20;

请尝试去掉你要跨链的金额中的小数点后的数字。



#### 按钮显示 "没有足够的原生代币作为 gas （**not enough native for gas）**"

请注意，要将 CAKE 发送到目的地链上的钱包。执行者（executor ）需要花费 gas。gas 费用将通过跨链 tx 收取源链的原生代币作为 gas：

* BNB 链 - BNB
* 以太链 - ETH
* Aptos 链 - APT

因此，如果你的源链钱包里没有足够的原生代币，你就不能执行跨链。&#x20;

如果你的目标地址已经拥有足够用的目的链原生代币，你可以关闭 "gas on destination"。



#### 我可以从BNB链跨链到以太链的不同的地址吗？&#x20;

不，你不可以。&#x20;

为了避免用户操作错误，在操作 EVM 类型公链之间的跨链时，目標鏈與源鏈必須使用同一地址。



#### 为什么按钮上显示 "X CAKE Exceeded"？&#x20;

为了安全起见，BSC 和 Aptos 之间每天可以跨链多少 CAKE 是有容量限制的。如果遇到这个问题，请减少 CAKE 的数量再次尝试，或者换个时间再度尝试。&#x20;

大厨们会根据需求动态调整这个限制。



#### 如果链上操作卡在 "Pending 待处理" 状态该怎么办？&#x20;

跨链交易将需要 30 分钟的时间来处理。请耐心等待，您可以在 [LayerZero scan](https://layerzeroscan.com/) 中输入交易的哈希值/ID 来搜索。&#x20;

如果 60 分钟后，跨链交易仍然显示为待处理。请通过我们的[社交渠道/群组](../../sheng-tai-xi-tong-he-zuo-huo-ban-guan-xi/contact-us/telegram.md)联系我们的管理员[寻求帮助](../../master/click-here-for-help/)。

&#x20;

#### 跨链操作后我一直没有收到我的 CAKE，怎么回事？&#x20;

跨链的链上操作将需要 30 分钟的时间来处理。请耐心等待，您可以在 [LayerZero scan](https://layerzeroscan.com/) 中输入交易的哈希值/ID 来搜索。&#x20;

当第一次将 CAKE 跨链到 Aptos 时，您必须手动领取您的 CAKE。请确保您已经启用了 "Gas on destination （获取目的地 gas）" ，或您的 Aptos 地址有足够的 APT 用于支付 gas。请查看此[指南](evm-lian-yu-aptos-zhi-jian-kua-lian.md)，了解跨链的详细步骤。&#x20;

将 CAKE 跨链到 BNB 智能链时，部分钱包程序需要手动添加 CAKE 代币合约地址到钱包，才能够查看余额。

如果您在跨链操作60分钟后还没有收到您的 CAKE，请通过我们的[社交渠道/群组](../../sheng-tai-xi-tong-he-zuo-huo-ban-guan-xi/contact-us/telegram.md)联系我们的管理员[寻求帮助](../../master/click-here-for-help/)。&#x20;



#### 为什么我不能跨链数量小于 0.00000001 的 CAKE？&#x20;

Aptos 上的代币最大小数点位数为 8 位，这也适用于 Aptos 上的 CAKE 代币。因此，当您将 CAKE 跨链到 Aptos 时，总数量小于 0.00000001 的链上交易将被拒绝。跨链到以太坊也适用此规则。

如果您跨链的 CAKE 数量的小数点位数大于 8 位，任何小于 0.00000001 部分的数量将被四舍五入，忽略不计并且不会进行跨链。未跨链的部分数量将留在您的 BNB 智能链钱包里。