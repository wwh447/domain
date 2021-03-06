# SaveRegistrantProfile {#concept_dsm_tbc_b2b .concept}

创建或者保存域名信息模板。

## 请求参数 {#section_v4h_whc_b2b .section}

公共请求参数，详见[公共参数](intl.zh-CN/API 参考/调用方式/公共参数.md#)。

|名称|类型|是否必须|描述|
|:-|:-|:---|:-|
|Action|String|是|操作接口名，系统规定参数，取值：SaveRegistrantProfile。|
|RegistrantProfileId|Long|创建模板时为空，更新模板时必须|域名信息模板ID。|
|Telephone|String|创建模板时必须，更新模板时可选|电话。|
|DefaultRegistrantProfile|Boolean|创建模板时必须，更新模板时可选|是否默认模板。|
|Country|String|创建模板时必须，更新模板时可选|国家代码 如CN，US。|
|Province|String|创建模板时必须，更新模板时可选|省份。|
|TelArea|String|创建模板时必须，更新模板时可选|电话国家代码。|
|City|String|创建模板时必须，更新模板时可选|城市。|
|PostalCode|String|创建模板时必须，更新模板时可选|邮政编码。|
|Email|String|创建模板时必须，更新模板时可选|邮箱。|
|Address|String|创建模板时必须，更新模板时可选|具体的地址。|
|RegistrantName|String|创建模板时必须，更新模板时可选|联系人名称。|
|RegistrantOrganization|String|创建模板时必须，更新模板时可选|持有者名称。|
|TelExt|String|否|电话分机。|

## 返回参数 {#section_l6a_ed4_wod .section}

|名称|类型|描述|
|:-|:-|:-|
|RequestId|String|唯一请求识别码。|
|RegistrantProfileId|Long|联系人信息模板ID。|

## 错误码 {#section_v9g_9k0_633 .section}

|错误代码|描述|HTTP状态码|语义|
|:---|:-|:------|:-|
|ParameterIllegal|Parameter illegal.|400|参数错误|
|NetworkIOError|Network IO Error.|400|网络I/O异常|

## 示例 {#section_tpq_m3c_b2b .section}

**请求示例**

``` {#codeblock_num_ird_on6}
http://domain-intl.aliyuncs.com/?Action=SaveRegistrantProfile
&DefaultRegistrantProfile=false
&Email=a%40a.com
&Address=test+a
&Telephone=18800000000
&PostalCode=000000
&City=testc
&Province=test+p
&RegistrantName=test+rn
&Country=CN
&RegistrantOrganization=test+ro
&TelArea=86
&<公共请求参数>
```

**返回示例**

-   XML示例

    ``` {#codeblock_8j8_5g7_qcp}
    <?xml version='1.0' encoding='UTF-8'?>
    <SaveRegistrantProfileResponse>
        <RegistrantProfileId>3600000</RegistrantProfileId>
        <RequestId>D09B153B-294D-42F1-BB61-F1C72136DFD3</RequestId>
    </SaveRegistrantProfileResponse>
    ```

-   JSON示例

    ``` {#codeblock_vhz_kl0_fhn}
    {
      "RegistrantProfileId": "3696573",
      "RequestId": "ECB708B9-A82E-45D7-A230-58231E532A57"
    }
    ```


