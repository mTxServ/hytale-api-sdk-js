# HytaleApi.ArticlesApi

All URIs are relative to *http://hytale.com/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getArticleBySlug**](ArticlesApi.md#getArticleBySlug) | **GET** /blog/post/slug/{slug} | 
[**getArticles**](ArticlesApi.md#getArticles) | **GET** /blog/post/published | 
[**getArticlesOfMonthAndYear**](ArticlesApi.md#getArticlesOfMonthAndYear) | **GET** /blog/post/archive/{year}/{month}/ | 


<a name="getArticleBySlug"></a>
# **getArticleBySlug**
> Article getArticleBySlug(slug)



Get list of articles published

### Example
```javascript
var HytaleApi = require('hytale-api-sdk');

var apiInstance = new HytaleApi.ArticlesApi();

var slug = "slug_example"; // String | Slug of article


var callback = function(error, data, response) {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
};
apiInstance.getArticleBySlug(slug, callback);
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **slug** | **String**| Slug of article | 

### Return type

[**Article**](Article.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a name="getArticles"></a>
# **getArticles**
> [Article] getArticles(opts)



Get list of articles published

### Example
```javascript
var HytaleApi = require('hytale-api-sdk');

var apiInstance = new HytaleApi.ArticlesApi();

var opts = { 
  'featuredOnly': true // Boolean | 
};

var callback = function(error, data, response) {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
};
apiInstance.getArticles(opts, callback);
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **featuredOnly** | **Boolean**|  | [optional] 

### Return type

[**[Article]**](Article.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a name="getArticlesOfMonthAndYear"></a>
# **getArticlesOfMonthAndYear**
> [Article] getArticlesOfMonthAndYear(year, month)



Get list of articles published on a specific month of an year

### Example
```javascript
var HytaleApi = require('hytale-api-sdk');

var apiInstance = new HytaleApi.ArticlesApi();

var year = 56; // Number | Year (ex: 2019)

var month = 56; // Number | Month (ex: 01)


var callback = function(error, data, response) {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
};
apiInstance.getArticlesOfMonthAndYear(year, month, callback);
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **year** | **Number**| Year (ex: 2019) | 
 **month** | **Number**| Month (ex: 01) | 

### Return type

[**[Article]**](Article.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

