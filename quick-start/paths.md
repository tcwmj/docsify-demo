
<a name="paths"></a>
## Paths

<a name="createcontractusingpost"></a>
### 创建合同
```
POST /{tenantId}/enterprise/v1/econtract/contracts
```


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Header**|**x-userinfo**  <br>*optional*|用户信息|string|
|**Path**|**tenantId**  <br>*required*|租户id|integer(int64)|
|**Query**|**appId**  <br>*required*|应用id|integer(int64)|
|**Query**|**companyId**  <br>*required*|公司id|integer(int64)|
|**Body**|**contractCreationRequest**  <br>*required*|创建合同请求|[ContractCreationRequest](#contractcreationrequest)|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|OK|[DefaultResponse](#defaultresponse)|
|**201**|Created|No Content|
|**401**|Unauthorized|No Content|
|**403**|Forbidden|No Content|
|**404**|Not Found|No Content|


#### Consumes

* `application/json;charset=UTF-8`


#### Produces

* `application/json;charset=UTF-8`


#### Tags

* electronic contract


<a name="uploadtemplateusingpost"></a>
### 上传合同模板
```
POST /{tenantId}/enterprise/v1/econtract/contracts/templates
```


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Header**|**x-userinfo**  <br>*optional*|用户信息|string|
|**Path**|**tenantId**  <br>*required*|租户id|integer(int64)|
|**Query**|**appId**  <br>*required*|应用id|integer(int64)|
|**Query**|**companyId**  <br>*required*|公司id|integer(int64)|
|**FormData**|**multipartFile**  <br>*required*|合同模板文件|file|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|OK|[DefaultResponse](#defaultresponse)|
|**201**|Created|No Content|
|**401**|Unauthorized|No Content|
|**403**|Forbidden|No Content|
|**404**|Not Found|No Content|


#### Consumes

* `multipart/form-data`


#### Produces

* `application/json;charset=UTF-8`


#### Tags

* electronic contract


<a name="obtaincontractusingget"></a>
### 获取合同
```
GET /{tenantId}/enterprise/v1/econtract/contracts/{contractId}
```


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Header**|**x-userinfo**  <br>*optional*|用户信息|string|
|**Path**|**contractId**  <br>*required*|合同id|string|
|**Path**|**tenantId**  <br>*required*|租户id|integer(int64)|
|**Query**|**appId**  <br>*required*|应用id|integer(int64)|
|**Query**|**companyId**  <br>*required*|公司id|integer(int64)|
|**Query**|**download**  <br>*required*|是否需要下载|boolean|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|OK|[DefaultResponse](#defaultresponse)|
|**401**|Unauthorized|No Content|
|**403**|Forbidden|No Content|
|**404**|Not Found|No Content|


#### Produces

* `application/json;charset=UTF-8`


#### Tags

* electronic contract


<a name="signcontractusingpost"></a>
### 签署合同
```
POST /{tenantId}/enterprise/v1/econtract/contracts/{contractId}/signature
```


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Header**|**x-userinfo**  <br>*optional*|用户信息|string|
|**Path**|**contractId**  <br>*required*|合同id|string|
|**Path**|**tenantId**  <br>*required*|租户id|integer(int64)|
|**Query**|**appId**  <br>*required*|应用id|integer(int64)|
|**Query**|**auto**  <br>*required*|是否自动签署|boolean|
|**Query**|**companyId**  <br>*required*|公司id|integer(int64)|
|**Body**|**contractSignRequest**  <br>*required*|签署合同请求|[ContractSignRequest](#contractsignrequest)|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|OK|[DefaultResponse](#defaultresponse)|
|**201**|Created|No Content|
|**401**|Unauthorized|No Content|
|**403**|Forbidden|No Content|
|**404**|Not Found|No Content|


#### Consumes

* `application/json;charset=UTF-8`


#### Produces

* `application/json;charset=UTF-8`


#### Tags

* electronic contract


<a name="uploadsealusingpost"></a>
### 上传签章文字或图片
```
POST /{tenantId}/enterprise/v1/econtract/seals
```


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Header**|**x-userinfo**  <br>*optional*|用户信息|string|
|**Path**|**tenantId**  <br>*required*|租户id|integer(int64)|
|**Query**|**appId**  <br>*required*|应用id|integer(int64)|
|**Query**|**companyId**  <br>*required*|公司id|integer(int64)|
|**Body**|**sealUploadRequest**  <br>*required*|签章上传请求|[SealUploadRequest](#sealuploadrequest)|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|OK|[DefaultResponse](#defaultresponse)|
|**201**|Created|No Content|
|**401**|Unauthorized|No Content|
|**403**|Forbidden|No Content|
|**404**|Not Found|No Content|


#### Consumes

* `application/json;charset=UTF-8`


#### Produces

* `application/json;charset=UTF-8`


#### Tags

* electronic seal



