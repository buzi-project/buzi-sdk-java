# SmsApi

All URIs are relative to *https://petstore3.swagger.io*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**cancelMessage**](SmsApi.md#cancelMessage) | **POST** /v1/sms/messages/{messageId}/cancel | Cancel a message |
| [**createMessage**](SmsApi.md#createMessage) | **POST** /v1/sms/messages | Create Message |
| [**createPricing**](SmsApi.md#createPricing) | **PUT** /v1/sms/networks/{networkId}/pricing | Create network price |
| [**deleteMessage**](SmsApi.md#deleteMessage) | **DELETE** /v1/sms/messages/{messageId} | Deletes a message |
| [**getMessage**](SmsApi.md#getMessage) | **GET** /v1/sms/messages/{messageId} | Get message |
| [**getNetwork**](SmsApi.md#getNetwork) | **GET** /v1/sms/networks/{networkId} | Get network |
| [**getPricing**](SmsApi.md#getPricing) | **GET** /v1/sms/networks/{networkId}/pricing | List network rates |
| [**listMessages**](SmsApi.md#listMessages) | **GET** /v1/sms/messages | List messages |
| [**listNetworks**](SmsApi.md#listNetworks) | **GET** /v1/sms/networks | List networks |
| [**sendMessage**](SmsApi.md#sendMessage) | **POST** /v1/sms/messages/{messageId}/send | Sends a message |


<a name="cancelMessage"></a>
# **cancelMessage**
> Message cancelMessage(messageId)

Cancel a message

Returns a single pet

### Example
```java
// Import classes:
import io.gitlab.buziproject.v2.ApiClient;
import io.gitlab.buziproject.v2.ApiException;
import io.gitlab.buziproject.v2.Configuration;
import io.gitlab.buziproject.v2.auth.*;
import io.gitlab.buziproject.v2.models.*;
import io.gitlab.buziproject.v2.SmsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBaseUrl("https://petstore3.swagger.io");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    // Configure HTTP basic authorization: BasicAuth
    HttpBasicAuth BasicAuth = (HttpBasicAuth) defaultClient.getAuthentication("BasicAuth");
    BasicAuth.setUsername("YOUR USERNAME");
    BasicAuth.setPassword("YOUR PASSWORD");

    // Configure HTTP bearer authorization: BearerAuth
    HttpBearerAuth BearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("BearerAuth");
    BearerAuth.setBearerToken("BEARER TOKEN");

    SmsApi apiInstance = new SmsApi(defaultClient);
    Long messageId = 56L; // Long | ID of pet to return
    try {
      Message result = apiInstance.cancelMessage(messageId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling SmsApi#cancelMessage");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **messageId** | **Long**| ID of pet to return | |

### Return type

[**Message**](Message.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BasicAuth](../README.md#BasicAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | successful operation |  -  |
| **400** | Invalid ID supplied |  -  |
| **404** | Pet not found |  -  |
| **0** | Unexpected Error |  -  |

<a name="createMessage"></a>
# **createMessage**
> Message createMessage(createMessageInput)

Create Message

Update an existing pet by Id

### Example
```java
// Import classes:
import io.gitlab.buziproject.v2.ApiClient;
import io.gitlab.buziproject.v2.ApiException;
import io.gitlab.buziproject.v2.Configuration;
import io.gitlab.buziproject.v2.auth.*;
import io.gitlab.buziproject.v2.models.*;
import io.gitlab.buziproject.v2.SmsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBaseUrl("https://petstore3.swagger.io");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    // Configure HTTP basic authorization: BasicAuth
    HttpBasicAuth BasicAuth = (HttpBasicAuth) defaultClient.getAuthentication("BasicAuth");
    BasicAuth.setUsername("YOUR USERNAME");
    BasicAuth.setPassword("YOUR PASSWORD");

    // Configure HTTP bearer authorization: BearerAuth
    HttpBearerAuth BearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("BearerAuth");
    BearerAuth.setBearerToken("BEARER TOKEN");

    SmsApi apiInstance = new SmsApi(defaultClient);
    CreateMessageInput createMessageInput = new CreateMessageInput(); // CreateMessageInput | Update an existent pet in the store
    try {
      Message result = apiInstance.createMessage(createMessageInput);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling SmsApi#createMessage");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **createMessageInput** | [**CreateMessageInput**](CreateMessageInput.md)| Update an existent pet in the store | |

### Return type

[**Message**](Message.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BasicAuth](../README.md#BasicAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful operation |  -  |
| **400** | Invalid ID supplied |  -  |
| **404** | Pet not found |  -  |
| **405** | Validation exception |  -  |
| **0** | Unexpected Error |  -  |

<a name="createPricing"></a>
# **createPricing**
> Message createPricing(networkId)

Create network price

Returns a single pet

### Example
```java
// Import classes:
import io.gitlab.buziproject.v2.ApiClient;
import io.gitlab.buziproject.v2.ApiException;
import io.gitlab.buziproject.v2.Configuration;
import io.gitlab.buziproject.v2.auth.*;
import io.gitlab.buziproject.v2.models.*;
import io.gitlab.buziproject.v2.SmsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBaseUrl("https://petstore3.swagger.io");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    // Configure HTTP basic authorization: BasicAuth
    HttpBasicAuth BasicAuth = (HttpBasicAuth) defaultClient.getAuthentication("BasicAuth");
    BasicAuth.setUsername("YOUR USERNAME");
    BasicAuth.setPassword("YOUR PASSWORD");

    // Configure HTTP bearer authorization: BearerAuth
    HttpBearerAuth BearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("BearerAuth");
    BearerAuth.setBearerToken("BEARER TOKEN");

    SmsApi apiInstance = new SmsApi(defaultClient);
    Integer networkId = 56; // Integer | 
    try {
      Message result = apiInstance.createPricing(networkId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling SmsApi#createPricing");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **networkId** | **Integer**|  | |

### Return type

[**Message**](Message.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BasicAuth](../README.md#BasicAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | successful operation |  -  |
| **400** | Invalid ID supplied |  -  |
| **404** | Pet not found |  -  |
| **0** | Unexpected Error |  -  |

<a name="deleteMessage"></a>
# **deleteMessage**
> Error deleteMessage(messageId, apiKey)

Deletes a message

delete a message

### Example
```java
// Import classes:
import io.gitlab.buziproject.v2.ApiClient;
import io.gitlab.buziproject.v2.ApiException;
import io.gitlab.buziproject.v2.Configuration;
import io.gitlab.buziproject.v2.auth.*;
import io.gitlab.buziproject.v2.models.*;
import io.gitlab.buziproject.v2.SmsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBaseUrl("https://petstore3.swagger.io");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    // Configure HTTP basic authorization: BasicAuth
    HttpBasicAuth BasicAuth = (HttpBasicAuth) defaultClient.getAuthentication("BasicAuth");
    BasicAuth.setUsername("YOUR USERNAME");
    BasicAuth.setPassword("YOUR PASSWORD");

    // Configure HTTP bearer authorization: BearerAuth
    HttpBearerAuth BearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("BearerAuth");
    BearerAuth.setBearerToken("BEARER TOKEN");

    SmsApi apiInstance = new SmsApi(defaultClient);
    Long messageId = 56L; // Long | Pet id to delete
    String apiKey = "apiKey_example"; // String | 
    try {
      Error result = apiInstance.deleteMessage(messageId, apiKey);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling SmsApi#deleteMessage");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **messageId** | **Long**| Pet id to delete | |
| **apiKey** | **String**|  | [optional] |

### Return type

[**Error**](Error.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BasicAuth](../README.md#BasicAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **400** | Invalid pet value |  -  |
| **0** | Unexpected Error |  -  |

<a name="getMessage"></a>
# **getMessage**
> Message getMessage(messageId)

Get message

Returns a single pet

### Example
```java
// Import classes:
import io.gitlab.buziproject.v2.ApiClient;
import io.gitlab.buziproject.v2.ApiException;
import io.gitlab.buziproject.v2.Configuration;
import io.gitlab.buziproject.v2.auth.*;
import io.gitlab.buziproject.v2.models.*;
import io.gitlab.buziproject.v2.SmsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBaseUrl("https://petstore3.swagger.io");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    // Configure HTTP basic authorization: BasicAuth
    HttpBasicAuth BasicAuth = (HttpBasicAuth) defaultClient.getAuthentication("BasicAuth");
    BasicAuth.setUsername("YOUR USERNAME");
    BasicAuth.setPassword("YOUR PASSWORD");

    // Configure HTTP bearer authorization: BearerAuth
    HttpBearerAuth BearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("BearerAuth");
    BearerAuth.setBearerToken("BEARER TOKEN");

    SmsApi apiInstance = new SmsApi(defaultClient);
    Long messageId = 56L; // Long | ID of pet to return
    try {
      Message result = apiInstance.getMessage(messageId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling SmsApi#getMessage");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **messageId** | **Long**| ID of pet to return | |

### Return type

[**Message**](Message.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BasicAuth](../README.md#BasicAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | successful operation |  -  |
| **400** | Invalid ID supplied |  -  |
| **404** | Pet not found |  -  |
| **0** | Unexpected Error |  -  |

<a name="getNetwork"></a>
# **getNetwork**
> Network getNetwork(networkId, countryCode)

Get network

Returns a single pet

### Example
```java
// Import classes:
import io.gitlab.buziproject.v2.ApiClient;
import io.gitlab.buziproject.v2.ApiException;
import io.gitlab.buziproject.v2.Configuration;
import io.gitlab.buziproject.v2.auth.*;
import io.gitlab.buziproject.v2.models.*;
import io.gitlab.buziproject.v2.SmsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBaseUrl("https://petstore3.swagger.io");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    // Configure HTTP basic authorization: BasicAuth
    HttpBasicAuth BasicAuth = (HttpBasicAuth) defaultClient.getAuthentication("BasicAuth");
    BasicAuth.setUsername("YOUR USERNAME");
    BasicAuth.setPassword("YOUR PASSWORD");

    // Configure HTTP bearer authorization: BearerAuth
    HttpBearerAuth BearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("BearerAuth");
    BearerAuth.setBearerToken("BEARER TOKEN");

    SmsApi apiInstance = new SmsApi(defaultClient);
    Integer networkId = 56; // Integer | 
    Long countryCode = 56L; // Long | ID of pet to return
    try {
      Network result = apiInstance.getNetwork(networkId, countryCode);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling SmsApi#getNetwork");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **networkId** | **Integer**|  | |
| **countryCode** | **Long**| ID of pet to return | [optional] |

### Return type

[**Network**](Network.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BasicAuth](../README.md#BasicAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | successful operation |  -  |
| **400** | Invalid ID supplied |  -  |
| **404** | Pet not found |  -  |
| **0** | Unexpected Error |  -  |

<a name="getPricing"></a>
# **getPricing**
> List&lt;Pricing&gt; getPricing(networkId)

List network rates

Returns a single pet

### Example
```java
// Import classes:
import io.gitlab.buziproject.v2.ApiClient;
import io.gitlab.buziproject.v2.ApiException;
import io.gitlab.buziproject.v2.Configuration;
import io.gitlab.buziproject.v2.auth.*;
import io.gitlab.buziproject.v2.models.*;
import io.gitlab.buziproject.v2.SmsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBaseUrl("https://petstore3.swagger.io");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    // Configure HTTP basic authorization: BasicAuth
    HttpBasicAuth BasicAuth = (HttpBasicAuth) defaultClient.getAuthentication("BasicAuth");
    BasicAuth.setUsername("YOUR USERNAME");
    BasicAuth.setPassword("YOUR PASSWORD");

    // Configure HTTP bearer authorization: BearerAuth
    HttpBearerAuth BearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("BearerAuth");
    BearerAuth.setBearerToken("BEARER TOKEN");

    SmsApi apiInstance = new SmsApi(defaultClient);
    Integer networkId = 56; // Integer | 
    try {
      List<Pricing> result = apiInstance.getPricing(networkId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling SmsApi#getPricing");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **networkId** | **Integer**|  | |

### Return type

[**List&lt;Pricing&gt;**](Pricing.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BasicAuth](../README.md#BasicAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | successful operation |  -  |
| **400** | Invalid ID supplied |  -  |
| **404** | Pet not found |  -  |
| **0** | Unexpected Error |  -  |

<a name="listMessages"></a>
# **listMessages**
> List&lt;Message&gt; listMessages(inbox, status)

List messages

Update an existing pet by Id

### Example
```java
// Import classes:
import io.gitlab.buziproject.v2.ApiClient;
import io.gitlab.buziproject.v2.ApiException;
import io.gitlab.buziproject.v2.Configuration;
import io.gitlab.buziproject.v2.auth.*;
import io.gitlab.buziproject.v2.models.*;
import io.gitlab.buziproject.v2.SmsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBaseUrl("https://petstore3.swagger.io");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    // Configure HTTP basic authorization: BasicAuth
    HttpBasicAuth BasicAuth = (HttpBasicAuth) defaultClient.getAuthentication("BasicAuth");
    BasicAuth.setUsername("YOUR USERNAME");
    BasicAuth.setPassword("YOUR PASSWORD");

    // Configure HTTP bearer authorization: BearerAuth
    HttpBearerAuth BearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("BearerAuth");
    BearerAuth.setBearerToken("BEARER TOKEN");

    SmsApi apiInstance = new SmsApi(defaultClient);
    String inbox = "inbox_example"; // String | 
    String status = "status_example"; // String | 
    try {
      List<Message> result = apiInstance.listMessages(inbox, status);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling SmsApi#listMessages");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **inbox** | **String**|  | [optional] |
| **status** | **String**|  | [optional] |

### Return type

[**List&lt;Message&gt;**](Message.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BasicAuth](../README.md#BasicAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful operation |  -  |
| **400** | Invalid ID supplied |  -  |
| **404** | Pet not found |  -  |
| **405** | Validation exception |  -  |
| **0** | Unexpected Error |  -  |

<a name="listNetworks"></a>
# **listNetworks**
> List&lt;Network&gt; listNetworks(countryCode)

List networks

Returns a single pet

### Example
```java
// Import classes:
import io.gitlab.buziproject.v2.ApiClient;
import io.gitlab.buziproject.v2.ApiException;
import io.gitlab.buziproject.v2.Configuration;
import io.gitlab.buziproject.v2.auth.*;
import io.gitlab.buziproject.v2.models.*;
import io.gitlab.buziproject.v2.SmsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBaseUrl("https://petstore3.swagger.io");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    // Configure HTTP basic authorization: BasicAuth
    HttpBasicAuth BasicAuth = (HttpBasicAuth) defaultClient.getAuthentication("BasicAuth");
    BasicAuth.setUsername("YOUR USERNAME");
    BasicAuth.setPassword("YOUR PASSWORD");

    // Configure HTTP bearer authorization: BearerAuth
    HttpBearerAuth BearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("BearerAuth");
    BearerAuth.setBearerToken("BEARER TOKEN");

    SmsApi apiInstance = new SmsApi(defaultClient);
    String countryCode = "countryCode_example"; // String | ID of pet to return
    try {
      List<Network> result = apiInstance.listNetworks(countryCode);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling SmsApi#listNetworks");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **countryCode** | **String**| ID of pet to return | [optional] |

### Return type

[**List&lt;Network&gt;**](Network.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BasicAuth](../README.md#BasicAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | successful operation |  -  |
| **400** | Invalid ID supplied |  -  |
| **404** | Pet not found |  -  |
| **0** | Unexpected Error |  -  |

<a name="sendMessage"></a>
# **sendMessage**
> Message sendMessage(messageId)

Sends a message

Returns a single pet

### Example
```java
// Import classes:
import io.gitlab.buziproject.v2.ApiClient;
import io.gitlab.buziproject.v2.ApiException;
import io.gitlab.buziproject.v2.Configuration;
import io.gitlab.buziproject.v2.auth.*;
import io.gitlab.buziproject.v2.models.*;
import io.gitlab.buziproject.v2.SmsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBaseUrl("https://petstore3.swagger.io");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    // Configure HTTP basic authorization: BasicAuth
    HttpBasicAuth BasicAuth = (HttpBasicAuth) defaultClient.getAuthentication("BasicAuth");
    BasicAuth.setUsername("YOUR USERNAME");
    BasicAuth.setPassword("YOUR PASSWORD");

    // Configure HTTP bearer authorization: BearerAuth
    HttpBearerAuth BearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("BearerAuth");
    BearerAuth.setBearerToken("BEARER TOKEN");

    SmsApi apiInstance = new SmsApi(defaultClient);
    Long messageId = 56L; // Long | ID of pet to return
    try {
      Message result = apiInstance.sendMessage(messageId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling SmsApi#sendMessage");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **messageId** | **Long**| ID of pet to return | |

### Return type

[**Message**](Message.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [BasicAuth](../README.md#BasicAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | successful operation |  -  |
| **400** | Invalid ID supplied |  -  |
| **404** | Pet not found |  -  |
| **0** | Unexpected Error |  -  |

