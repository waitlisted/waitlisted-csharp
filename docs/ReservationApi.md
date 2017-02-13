# IO.Swagger.Api.ReservationApi

All URIs are relative to *https://www.waitlisted.co/api/v2*

Method | HTTP request | Description
------------- | ------------- | -------------
[**ActivateReservation**](ReservationApi.md#activatereservation) | **POST** /reservations/activate | 
[**CreateReservation**](ReservationApi.md#createreservation) | **POST** /reservations | 
[**DeleteReservation**](ReservationApi.md#deletereservation) | **DELETE** /reservations | 
[**GetReservation**](ReservationApi.md#getreservation) | **GET** /reservations | 


<a name="activatereservation"></a>
# **ActivateReservation**
> ReservationsResponse ActivateReservation (ReservationRequest body)



Activate a reservation.

### Example
```csharp
using System;
using System.Diagnostics;
using IO.Swagger.Api;
using IO.Swagger.Client;
using IO.Swagger.Model;

namespace Example
{
    public class ActivateReservationExample
    {
        public void main()
        {
            
            // Configure API key authorization: api_key
            Configuration.Default.ApiKey.Add("X-API-Key", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // Configuration.Default.ApiKeyPrefix.Add("X-API-Key", "Bearer");

            var apiInstance = new ReservationApi();
            var body = new ReservationRequest(); // ReservationRequest | Reservation Data

            try
            {
                ReservationsResponse result = apiInstance.ActivateReservation(body);
                Debug.WriteLine(result);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling ReservationApi.ActivateReservation: " + e.Message );
            }
        }
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**ReservationRequest**](ReservationRequest.md)| Reservation Data | 

### Return type

[**ReservationsResponse**](ReservationsResponse.md)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a name="createreservation"></a>
# **CreateReservation**
> ReservationsResponse CreateReservation (Reservation body)



Creates a new reservation.

### Example
```csharp
using System;
using System.Diagnostics;
using IO.Swagger.Api;
using IO.Swagger.Client;
using IO.Swagger.Model;

namespace Example
{
    public class CreateReservationExample
    {
        public void main()
        {
            
            var apiInstance = new ReservationApi();
            var body = new Reservation(); // Reservation | Reservation Data

            try
            {
                ReservationsResponse result = apiInstance.CreateReservation(body);
                Debug.WriteLine(result);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling ReservationApi.CreateReservation: " + e.Message );
            }
        }
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**Reservation**](Reservation.md)| Reservation Data | 

### Return type

[**ReservationsResponse**](ReservationsResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a name="deletereservation"></a>
# **DeleteReservation**
> void DeleteReservation (ReservationRequest body)



Delete a reservation.

### Example
```csharp
using System;
using System.Diagnostics;
using IO.Swagger.Api;
using IO.Swagger.Client;
using IO.Swagger.Model;

namespace Example
{
    public class DeleteReservationExample
    {
        public void main()
        {
            
            // Configure API key authorization: api_key
            Configuration.Default.ApiKey.Add("X-API-Key", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // Configuration.Default.ApiKeyPrefix.Add("X-API-Key", "Bearer");

            var apiInstance = new ReservationApi();
            var body = new ReservationRequest(); // ReservationRequest | Reservation Data

            try
            {
                apiInstance.DeleteReservation(body);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling ReservationApi.DeleteReservation: " + e.Message );
            }
        }
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**ReservationRequest**](ReservationRequest.md)| Reservation Data | 

### Return type

void (empty response body)

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a name="getreservation"></a>
# **GetReservation**
> ReservationsResponse GetReservation (string email)



Get a reservation.

### Example
```csharp
using System;
using System.Diagnostics;
using IO.Swagger.Api;
using IO.Swagger.Client;
using IO.Swagger.Model;

namespace Example
{
    public class GetReservationExample
    {
        public void main()
        {
            
            var apiInstance = new ReservationApi();
            var email = email_example;  // string | Email address

            try
            {
                ReservationsResponse result = apiInstance.GetReservation(email);
                Debug.WriteLine(result);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling ReservationApi.GetReservation: " + e.Message );
            }
        }
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **email** | **string**| Email address | 

### Return type

[**ReservationsResponse**](ReservationsResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

