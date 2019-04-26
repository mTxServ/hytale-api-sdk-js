# HytaleApi.JobsApi

All URIs are relative to *http://hytale.com/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getJobs**](JobsApi.md#getJobs) | **GET** /job/listing | 


<a name="getJobs"></a>
# **getJobs**
> [Job] getJobs()



Get list of jobs

### Example
```javascript
var HytaleApi = require('hytale-api-sdk');

var apiInstance = new HytaleApi.JobsApi();

var callback = function(error, data, response) {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
};
apiInstance.getJobs(callback);
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**[Job]**](Job.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

