
    
**简要描述：** 

- 身份认证接口

**请求URL：** 
- ` http://160.161.12.120：12025/ `
  
**请求方式：**
- POST 

**参数：** 

|参数|必选|类型|长度|说明|默认值|
|:-------|:-------|:-------|:-------|:-------|:-------|
| tx_code|是 | string|6| 交易码 |GW9901|
| uuid |是| string|64| 唯一ID |&nbsp;|
| - cd |是|object  |0| 对象 |&nbsp;|
| - cd-mobileNo|是 | string|11| 手机号 |&nbsp;|
| - cd-interCode|是 | string|6| 接口代码 |&nbsp;|
| - cd-chnlCode|是 | string|6| 渠道代码 |1|
| - cd-certNo |是| string|6| 身份证号码 |&nbsp;|
| mac |是| string|6| mac校验 |&nbsp;||


 **请求示例**

``` 
  {
        "tx_code":"GW9901",
        "uuid":"",
		"cd":{
			"interCode": "0210000903",
        	"chnlCode":"1",
			"mobileNo": "1380000000",
        	"certNo":"6231789946660111549"
					},
        "mac":"7F63D5FAAD29E7BD7D3399059E173A34"
  }
```


 **返回

``` 
  {
        "hostReturnCode":"0000",
        "tx_code":"GW9901",
        "uuid":"",
		"cd":{
			"uid":"",
			"name":"张飞",
			"dept":"公关部",
			"name":"16.00",
        	"certNo":"6231789946660111549"
			"mobileNo": "1380000000",
			"balance": "220.00",
		},
        "mac":"7F63D5FAAD29E7BD7D3399059E173A34",
        "hostErrorMessage":"交易成功"
  }
```

 **返回参数说明** 

|参数|必选|类型|长度|说明|默认值|
|:-------|:-------|:-------|:-------|:-------|:-------|
| - cd |是|object  |0| 对象 |&nbsp;|
| - cd-uid |是| string|64| 识别号 |&nbsp;|
| - cd-certNo |是| string|6| 身份证号码 |&nbsp;|
| - cd-name|是 | string|50| 姓名 |&nbsp;|
| - cd-dept|是 | string|50| 部门 |&nbsp;|
| - cd-balance|是 | string|18| 饭卡余额 |0.00|
|hostReturnCode |是 |String |6 |返回值：0000成功，其他为失败|&nbsp; &nbsp; &nbsp;  |
|hostErrorMessage |是 |String |60 |交易信息|&nbsp; &nbsp; &nbsp;  |

 **备注** 

- 更多返回错误代码请看首页的错误代码描述

