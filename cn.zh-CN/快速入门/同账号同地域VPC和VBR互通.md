# 同账号同地域VPC和VBR互通 {#concept_u15_r3b_tdb .concept}

本教程指引您如何使用云企业网实现同账号同地域下的网络实例互通。

## 前提条件 {#section_s15_w3b_tdb .section}

-   已创建VPC或VBR。

-   要互联的VPC和VBR实例没有使用高速通道。


## 步骤一 创建云企业网实例 {#section_snn_y3b_tdb .section}

1.  登录[云企业网管理控制台](https://cen.console.aliyun.com/)。
2.  在云企业网实例页面，单击创建云企业网实例。
3.  配置云企业网实例：
    -   **名称**：云企业网实例的名称。名称在2-128个字符之间，以英文字母或中文开始，可包含数字，连字符（-）和下划线（\_）。本操作输入**同账号同地域**。
    -   **加载网络实例**：

        -   **账号**：选择**同账号**。
        -   **实例类型**：选择要互通的实例，支持加载专有网络和边界路由器实例。本操作输入**专有网络实例**。
        -   **地域**：选择所选实例的地域。本操作选择**华北1**。
        -   **实例**：选择要加载的实例。本操作选择一个VPC实例。

            ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/3044/859_zh-CN.png)


## 步骤二 加载网络实例 { .section}

1.  在云企业网实例页面，单击已创建的云企业网实例的**操作**列下的**管理**。

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/3044/860_zh-CN.png)

2.  在**加载网络实例**页面，单击**加载网络实例**，配置网络实例：
    -   **账号**：选择**同账号**。
    -   **实例类型**：选择要互通的实例，支持加载专有网络和边界路由器实例。本操作选择**专有网络实例**。
    -   **地域**：选择所选实例的地域。本操作选择**华北1**。
    -   **实例**：选择要加载的实例。本操作选择一个VPC实例。

        ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/3044/5956_zh-CN.png)


## 步骤三 互通验证 {#section_ucp_y3b_tdb .section}

您可以登录到已加载的网络实例的内的任何一台ECS实例，然后使用ping命令，ping其他已加载的网络实例内的ECS实例的私网IP，查看是否互通。

**注：** 确保ECS实例的安全组中配置了相应的授权规则。

