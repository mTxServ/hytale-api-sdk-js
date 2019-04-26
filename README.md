# Hytale API - Javascript SDK

Hytale Api - JavaScript client for Hytale Official API

For more information, please visit [https://hytale.game](https://hytale.game)

## Installation

### For [Node.js](https://nodejs.org/)

#### npm

To publish the library as a [npm](https://www.npmjs.com/),
please follow the procedure in ["Publishing npm packages"](https://docs.npmjs.com/getting-started/publishing-npm-packages).

Then install it via:

```shell
npm install hytale-api-sdk --save
```

##### Local development

To use the library locally without publishing to a remote npm registry, first install the dependencies by changing 
into the directory containing `package.json` (and this README). Let's call this `JAVASCRIPT_CLIENT_DIR`. Then run:

```shell
npm install
```

Next, [link](https://docs.npmjs.com/cli/link) it globally in npm with the following, also from `JAVASCRIPT_CLIENT_DIR`:

```shell
npm link
```

Finally, switch to the directory you want to use your hytale_api from, and run:

```shell
npm link /path/to/<JAVASCRIPT_CLIENT_DIR>
```

You should now be able to `require('hytale_api')` in javascript files from the directory you ran the last 
command above from.

#### git
#
If the library is hosted at a git repository, e.g.
https://github.com/YOUR_USERNAME/hytale_api
then install it via:

```shell
    npm install YOUR_USERNAME/hytale_api --save
```

### For browser

The library also works in the browser environment via npm and [browserify](http://browserify.org/). After following
the above steps with Node.js and installing browserify with `npm install -g browserify`,
perform the following (assuming *main.js* is your entry file, that's to say your javascript file where you actually 
use this library):

```shell
browserify main.js > bundle.js
```

Then include *bundle.js* in the HTML pages.

### Webpack Configuration

Using Webpack you may encounter the following error: "Module not found: Error:
Cannot resolve module", most certainly you should disable AMD loader. Add/merge
the following section to your webpack config:

```javascript
module: {
  rules: [
    {
      parser: {
        amd: false
      }
    }
  ]
}
```

## Getting Started

Please follow the [installation](#installation) instruction and execute the following JS code:

```javascript
var HytaleApi = require('hytale_api');

var api = new HytaleApi.ArticlesApi()

var slug = "slug_example"; // {String} Slug of article


var callback = function(error, data, response) {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
};
api.getArticleBySlug(slug, callback);

```

## Documentation for API Endpoints

All URIs are relative to *https://hytale.com/api*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*HytaleApi.ArticlesApi* | [**getArticleBySlug**](docs/ArticlesApi.md#getArticleBySlug) | **GET** /blog/post/slug/{slug} | 
*HytaleApi.ArticlesApi* | [**getArticles**](docs/ArticlesApi.md#getArticles) | **GET** /blog/post/published | 
*HytaleApi.ArticlesApi* | [**getArticlesOfMonthAndYear**](docs/ArticlesApi.md#getArticlesOfMonthAndYear) | **GET** /blog/post/archive/{year}/{month}/ | 
*HytaleApi.JobsApi* | [**getJobs**](docs/JobsApi.md#getJobs) | **GET** /job/listing | 


## Documentation for Models

 - [HytaleApi.Article](docs/Article.md)
 - [HytaleApi.CoverImage](docs/CoverImage.md)
 - [HytaleApi.Job](docs/Job.md)


## Documentation for Authorization

 All endpoints do not require authorization.

