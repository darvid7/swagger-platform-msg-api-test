# swagger_client.AuthenticationApi

All URIs are relative to *https://tapi.telstra.com/v2*

Method | HTTP request | Description
------------- | ------------- | -------------
[**auth_token**](AuthenticationApi.md#auth_token) | **POST** /oauth/token | Generate OAuth2 token


# **auth_token**
> OAuthResponse auth_token(client_id, client_secret, grant_type)

Generate OAuth2 token

To generate an OAuth2 Authentication token, pass through your `Client key` and `Client secret` that you received when you registered for the &quot;API Free Trial&quot; Product.  The grant_type should be left as `client_credentials` and the scope as `NSMS`.  The token will expire in one hour. <pre><code class=\"language-sh\">   #!/bin/bash   # Obtain these keys from the Telstra Developer Portal   CLIENT_KEY=\"your client key\"   CLIENT_SECRET=\"your client secret\"   curl -X POST -H 'Content-Type: application/x-www-form-urlencoded' \\   -d 'grant_type=client_credentials&amp;client_id=$CLIENT_KEY&amp;client_secret=CLIENT_SECRET&amp;scope=NSMS' \\   'https://tapi.telstra.com/v2/oauth/token' </code></pre> 

### Example
```python
from __future__ import print_function
import time
import swagger_client
from swagger_client.rest import ApiException
from pprint import pprint

# create an instance of the API class
api_instance = swagger_client.AuthenticationApi()
client_id = 'client_id_example' # str | 
client_secret = 'client_secret_example' # str | 
grant_type = 'client_credentials' # str |  (default to client_credentials)

try:
    # Generate OAuth2 token
    api_response = api_instance.auth_token(client_id, client_secret, grant_type)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling AuthenticationApi->auth_token: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **client_id** | **str**|  | 
 **client_secret** | **str**|  | 
 **grant_type** | **str**|  | [default to client_credentials]

### Return type

[**OAuthResponse**](OAuthResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

