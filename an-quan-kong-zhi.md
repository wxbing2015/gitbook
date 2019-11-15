**MAC校验**

&nbsp; &nbsp;通讯报文组成如下格式

 ``` 
 { 
     "tx_code" : "", 
     "seqNo" : "1223", 
     "cd" : { 
          "acctNo" : "12345" 
     }, 
     "mac" : "40853A981092D87BAFB287A5B30BA801" 
 } 

 ```

对cd的值{"acctNo":"12345"}去空格，去不可见字符，然后计算mac值
然后对mac值前16位加密3des+mac后16位3des计算最终mac值
算法见源码。