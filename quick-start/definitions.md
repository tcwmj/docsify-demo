
<a name="definitions"></a>
## Definitions

<a name="contractcreationrequest"></a>
### ContractCreationRequest

|Name|Description|Schema|
|---|---|---|
|**contractTitle**  <br>*optional*|合同标题  <br>**Example** : `"XX投资合同"`|string|
|**dynamicTables**  <br>*optional*|动态表格|< string > array|
|**fontSize**  <br>*optional*|字体大小，参考word字体设置，例如：10,12.5,14  <br>**Example** : `"10"`|string|
|**fontType**  <br>*optional*|字体类型 0-宋体 1-仿宋 2-黑体 3-楷体 4-微软雅黑  <br>**Example** : `"0"`|string|
|**parameterMap**  <br>*optional*|合同参数|object|
|**templateId**  <br>*optional*|合同模板id  <br>**Example** : `"123456"`|string|


<a name="contractsignrequest"></a>
### ContractSignRequest

|Name|Description|Schema|
|---|---|---|
|**contractTitle**  <br>*optional*|合同标题  <br>**Example** : `"XX投资合同"`|string|
|**parameters**  <br>*optional*|自动签署可选参数|object|
|**sealId**  <br>*optional*|签章id，通过上传签章图片返回，注意上传签章文字不返回签章id）  <br>**Example** : `"123456"`|string|
|**transactionId**  <br>*optional*|自动签署事务id  <br>**Example** : `"123456"`|string|


<a name="defaultresponse"></a>
### DefaultResponse

|Name|Description|Schema|
|---|---|---|
|**code**  <br>*optional*|状态码  <br>**Example** : `"ELCCZZ0200"`|string|
|**message**  <br>*optional*|状态描述  <br>**Example** : `"请求成功"`|string|
|**result**  <br>*optional*|返回数据|object|


<a name="sealuploadrequest"></a>
### SealUploadRequest

|Name|Description|Schema|
|---|---|---|
|**sealBody**  <br>*optional*|签章文字内容（当sealBody非空时，sealImageBase64必须为空）  <br>**Example** : `"XXX公司"`|string|
|**sealImageBase64**  <br>*optional*|基于base64编码的电子签章图片（当sealImageBase64非空时，sealBody必须为空）  <br>**Example** : `"123456"`|string|



