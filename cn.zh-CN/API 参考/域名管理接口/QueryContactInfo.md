# QueryContactInfo {#concept_akb_ryk_c2b .concept}

QueryContactInfo：查询域名联系人信息。

## 请求参数 {#section_hcg_rtl_c2b .section}

公共请求参数，详见[公共参数](intl.zh-CN/API 参考/调用方式/公共参数.md#)。

|名称|类型|是否必须|描述|
|:-|:-|:---|:-|
|Action|String|是|操作接口名，系统规定参数，取值：QueryContactInfo。|
|DomainName|String|是|域名。|
|ContactType|String|是|联系人类型，可选值为：registrant 域名持有者；tech 技术者；admin 管理者；billing 付费者。|

## 返回参数 {#section_gk5_5tl_c2b .section}

|名称|类型|描述|
|:-|:-|:-|
|RequestId|String|唯一请求识别码。|
|CreateDate|String|创建时间。|
|RegistrantName|String|联系人名称。|
|RegistrantOrganization|String|持有者名称。|
|Province|String|省份。|
|City|String|城市。|
|Address|String|具体的地址。|
|Country|String|国家代码，如CN，US。|
|Email|String|邮箱。|
|PostalCode|String|邮政编码。|
|TelArea|String|电话国家代码。|
|Telephone|String|电话号码。|
|TelExt|String|分机号码。|

## 错误码 {#section_rxh_ddm_c2b .section}

|错误代码|描述|HTTP状态码|语义|
|:---|:-|:------|:-|
|ParameterIllegal|Parameter illegal.|400|参数错误。|
|NetworkIOError|Network IO Error.|400|网络I/O异常。|

## 示例 {#section_hb5_gdm_c2b .section}

**请求示例**

``` {#codeblock_xkn_zmr_1as}
http://domain-intl.aliyuncs.com/?Action=QueryContactInfo
&DomainName=fds234sdf.net&ContactType=admin
&<公共请求参数>
```

**返回示例**

-   XML示例

    ``` {#codeblock_tmq_eqc_rr7}
    <?xml version='1.0' encoding='UTF-8'?>
    <QueryContactInfoResponse>
        <CreateDate>2013-12-06 00:00:00</CreateDate>
        <Address>Ou Wo E Ou </Address>
        <TelExt></TelExt>
        <City>Bei Jing Shi</City>
        <Telephone>13000000000</Telephone>
        <Country>CN</Country>
        <TelArea>86</TelArea>
        <Province>Bei Jing</Province>
        <PostalCode>111111</PostalCode>
        <Email>13000000000@aliyun.com</Email>
        <RequestId>DBBEFD6C-86F2-4C68-930A-21F8668BB6E8</RequestId>
        <RegistrantName>li Yun</RegistrantName>
        <RegistrantOrganization>Li Yun</RegistrantOrganization>
    </QueryContactInfoResponse>
    ```

-   JSON示例

    ``` {#codeblock_371_qzl_az2}
    {
      "CreateDate": "2013-12-06 00:00:00",
      "Address": "Ou Wo E Ou ",
      "TelExt": "",
      "City": "Bei Jing Shi",
      "Telephone": "1300000000",
      "Country": "CN",
      "TelArea": "86",
      "Province": "Bei Jing",
      "PostalCode": "111111",
      "Email": "1300000000@aliyun.com",
      "RequestId": "77B19432-82FF-4D25-82F9-CF83E19516F7",
      "RegistrantName": "li Yun",
      "RegistrantOrganization": "Li Yun"
    }
    ```


