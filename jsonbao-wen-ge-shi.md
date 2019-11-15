
 **请求报文示例**

``` 
{
"tx_code": "CR1001",
"uuid":"",
    "cd": {
        "iCode": "0210000903",
        "cCode":"90880020",
        "idNumber":"6231789946660111549",
    },
    "mac": "3937f5733628b46afce79efe6359e615"
}
``` 
 **应答报文例子**
``` 
{
	"msgReturnFrom": "微信饭卡充值",
	"cd": {
		" uid ": "0210000903",
		" idNumber ": "6231789946660111549",
		"name ": "杨晞",
		" dept ": "部门",
		" balance ": "200.00"
	},
	"hostReturnCode": "0000",
	"tx_code": "CR1001",
	"uuid": "",
	"mac": "7F63D5FAAD29E7BD7D3399059E173A34",
	"hostErrorMessage": "交易成功"
}
``` 