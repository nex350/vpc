# 安全组与网络ACL区别<a name="zh-cn_topic_0052003963"></a>

通过配置网络ACL和安全组策略，保障VPC内的弹性云服务器安全使用。

-   安全组对弹性云服务器进行防护。
-   网络ACL对子网进行防护。

如[图1](#fig151401249216)所示。

**图 1**  安全组与网络ACL<a name="fig151401249216"></a>  
![](figures/安全组与网络ACL.png "安全组与网络ACL")

网络ACL和安全组区别如[表1](#table53053071174845)所示。

**表 1**  安全组和网络ACL

<a name="table53053071174845"></a>
<table><thead align="left"><tr id="row63488302174845"><th class="cellrowborder" valign="top" width="18.990000000000002%" id="mcps1.2.4.1.1"><p id="p16252192132814"><a name="p16252192132814"></a><a name="p16252192132814"></a>对比项</p>
</th>
<th class="cellrowborder" valign="top" width="35.8%" id="mcps1.2.4.1.2"><p id="p44965011174845"><a name="p44965011174845"></a><a name="p44965011174845"></a>安全组</p>
</th>
<th class="cellrowborder" valign="top" width="45.21%" id="mcps1.2.4.1.3"><p id="p18287275174845"><a name="p18287275174845"></a><a name="p18287275174845"></a>网络ACL</p>
</th>
</tr>
</thead>
<tbody><tr id="row30367752174845"><td class="cellrowborder" valign="top" width="18.990000000000002%" headers="mcps1.2.4.1.1 "><p id="p425252102818"><a name="p425252102818"></a><a name="p425252102818"></a>防护对象</p>
</td>
<td class="cellrowborder" valign="top" width="35.8%" headers="mcps1.2.4.1.2 "><p id="p43868882174845"><a name="p43868882174845"></a><a name="p43868882174845"></a>弹性云服务器级别操作。</p>
</td>
<td class="cellrowborder" valign="top" width="45.21%" headers="mcps1.2.4.1.3 "><p id="p63718581174845"><a name="p63718581174845"></a><a name="p63718581174845"></a>子网级别操作。</p>
</td>
</tr>
<tr id="row36596319174845"><td class="cellrowborder" valign="top" width="18.990000000000002%" headers="mcps1.2.4.1.1 "><p id="p9252182132813"><a name="p9252182132813"></a><a name="p9252182132813"></a>配置策略</p>
</td>
<td class="cellrowborder" valign="top" width="35.8%" headers="mcps1.2.4.1.2 "><p id="p11511833174845"><a name="p11511833174845"></a><a name="p11511833174845"></a>仅支持允许策略。</p>
</td>
<td class="cellrowborder" valign="top" width="45.21%" headers="mcps1.2.4.1.3 "><p id="p60043263174845"><a name="p60043263174845"></a><a name="p60043263174845"></a>支持允许、拒绝策略。</p>
</td>
</tr>
<tr id="row3518463174845"><td class="cellrowborder" valign="top" width="18.990000000000002%" headers="mcps1.2.4.1.1 "><p id="p3252321102813"><a name="p3252321102813"></a><a name="p3252321102813"></a>优先级</p>
</td>
<td class="cellrowborder" valign="top" width="35.8%" headers="mcps1.2.4.1.2 "><p id="p16560083174845"><a name="p16560083174845"></a><a name="p16560083174845"></a>多个规则冲突，取其并集生效。</p>
</td>
<td class="cellrowborder" valign="top" width="45.21%" headers="mcps1.2.4.1.3 "><p id="p66298376174845"><a name="p66298376174845"></a><a name="p66298376174845"></a>多个规则冲突，优先级高的规则优先生效。</p>
</td>
</tr>
<tr id="row59814478174845"><td class="cellrowborder" valign="top" width="18.990000000000002%" headers="mcps1.2.4.1.1 "><p id="p14252172117284"><a name="p14252172117284"></a><a name="p14252172117284"></a>应用操作</p>
</td>
<td class="cellrowborder" valign="top" width="35.8%" headers="mcps1.2.4.1.2 "><p id="p13134583174845"><a name="p13134583174845"></a><a name="p13134583174845"></a>创建弹性云服务器默认必须选择安全组，默认安全组自动应用到弹性云服务器。</p>
</td>
<td class="cellrowborder" valign="top" width="45.21%" headers="mcps1.2.4.1.3 "><p id="p57268308174845"><a name="p57268308174845"></a><a name="p57268308174845"></a>创建子网没有网络ACL选项，必须创建网络ACL、添加关联子网、添加出入规则，并启用网络ACL，才可应用到关联子网及子网下的弹性云服务器。</p>
</td>
</tr>
<tr id="row3289418310534"><td class="cellrowborder" valign="top" width="18.990000000000002%" headers="mcps1.2.4.1.1 "><p id="p82520212284"><a name="p82520212284"></a><a name="p82520212284"></a>报文组</p>
</td>
<td class="cellrowborder" valign="top" width="35.8%" headers="mcps1.2.4.1.2 "><p id="p4718316010534"><a name="p4718316010534"></a><a name="p4718316010534"></a>仅支持报文三元组（即协议、端口和对端地址）过滤。</p>
</td>
<td class="cellrowborder" valign="top" width="45.21%" headers="mcps1.2.4.1.3 "><p id="p6373958110534"><a name="p6373958110534"></a><a name="p6373958110534"></a>支持报文五元组（即协议、源端口、目的端口、源地址和目的地址）过滤。</p>
</td>
</tr>
</tbody>
</table>

