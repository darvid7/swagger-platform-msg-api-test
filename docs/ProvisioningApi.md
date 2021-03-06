# swagger_client.ProvisioningApi

All URIs are relative to *https://tapi.telstra.com/v2*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_subscription**](ProvisioningApi.md#create_subscription) | **POST** /messages/provisioning/subscriptions | Create Subscription
[**delete_subscription**](ProvisioningApi.md#delete_subscription) | **DELETE** /messages/provisioning/subscriptions | Delete Subscription
[**get_subscription**](ProvisioningApi.md#get_subscription) | **GET** /messages/provisioning/subscriptions | Get Subscription


# **create_subscription**
> ProvisionNumberResponse create_subscription(body)

Create Subscription

Invoke the provisioning API to get a dedicated mobile number for an account or application.  <pre><code class=\"language-sh\">   #!/bin/bash   curl -X POST \\   https://tapi.telstra.com/v2/messages/provisioning/subscriptions \\   -H 'authorization: Bearer $ACCESS_TOKEN' \\   -H 'cache-control: no-cache' \\   -H 'content-type: application/json' \\   -d '{   \"activeDays\":30,   \"notifyURL\":\"http://example.com/callback\",   \"callbackData\":     {       \"anything\":\"some data\"     }   }' </code></pre>

### Example
```python
from __future__ import print_function
import time
import swagger_client
from swagger_client.rest import ApiException
from pprint import pprint

# Configure OAuth2 access token for authorization: auth
configuration = swagger_client.Configuration()
configuration.access_token = 'YOUR_ACCESS_TOKEN'

# create an instance of the API class
api_instance = swagger_client.ProvisioningApi(swagger_client.ApiClient(configuration))
body = swagger_client.ProvisionNumberRequest() # ProvisionNumberRequest | A JSON payload containing the required attributes

try:
    # Create Subscription
    api_response = api_instance.create_subscription(body)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling ProvisioningApi->create_subscription: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**ProvisionNumberRequest**](ProvisionNumberRequest.md)| A JSON payload containing the required attributes | 

### Return type

[**ProvisionNumberResponse**](ProvisionNumberResponse.md)

### Authorization

[auth](../README.md#auth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_subscription**
> delete_subscription(body)

Delete Subscription

Delete a mobile number subscription from an account

### Example
```python
from __future__ import print_function
import time
import swagger_client
from swagger_client.rest import ApiException
from pprint import pprint

# Configure OAuth2 access token for authorization: auth
configuration = swagger_client.Configuration()
configuration.access_token = 'YOUR_ACCESS_TOKEN'

# create an instance of the API class
api_instance = swagger_client.ProvisioningApi(swagger_client.ApiClient(configuration))
body = swagger_client.DeleteNumberRequest() # DeleteNumberRequest | EmptyArr

try:
    # Delete Subscription
    api_instance.delete_subscription(body)
except ApiException as e:
    print("Exception when calling ProvisioningApi->delete_subscription: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**DeleteNumberRequest**](DeleteNumberRequest.md)| EmptyArr | 

### Return type

void (empty response body)

### Authorization

[auth](../README.md#auth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_subscription**
> GetSubscriptionResponse get_subscription()

Get Subscription

Get mobile number subscription for an account

### Example
```python
from __future__ import print_function
import time
import swagger_client
from swagger_client.rest import ApiException
from pprint import pprint

# Configure OAuth2 access token for authorization: auth
configuration = swagger_client.Configuration()
configuration.access_token = 'YOUR_ACCESS_TOKEN'

# create an instance of the API class
api_instance = swagger_client.ProvisioningApi(swagger_client.ApiClient(configuration))

try:
    # Get Subscription
    api_response = api_instance.get_subscription()
    pprint(api_response)
except ApiException as e:
    print("Exception when calling ProvisioningApi->get_subscription: %s\n" % e)
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**GetSubscriptionResponse**](GetSubscriptionResponse.md)

### Authorization

[auth](../README.md#auth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

