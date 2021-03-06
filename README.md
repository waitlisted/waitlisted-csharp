# IO.Swagger - the C# library for the Waitlisted API

Waitlisted API

This C# SDK is automatically generated by the [Swagger Codegen](https://github.com/swagger-api/swagger-codegen) project:

- API version: 2.0.0
- SDK version: 1.0.0
- Build date: 2017-02-12T22:31:59.137-06:00
- Build package: class io.swagger.codegen.languages.CSharpClientCodegen

## Frameworks supported
- .NET 4.0 or later
- Windows Phone 7.1 (Mango)

## Dependencies
- [RestSharp](https://www.nuget.org/packages/RestSharp) - 105.1.0 or later
- [Json.NET](https://www.nuget.org/packages/Newtonsoft.Json/) - 7.0.0 or later

The DLLs included in the package may not be the latest version. We recommned using [NuGet] (https://docs.nuget.org/consume/installing-nuget) to obtain the latest version of the packages:
```
Install-Package RestSharp
Install-Package Newtonsoft.Json
```

NOTE: RestSharp versions greater than 105.1.0 have a bug which causes file uploads to fail. See [RestSharp#742](https://github.com/restsharp/RestSharp/issues/742)

## Installation
Run the following command to generate the DLL
- [Mac/Linux] `/bin/sh build.sh`
- [Windows] `build.bat`

Then include the DLL (under the `bin` folder) in the C# project, and use the namespaces:
```csharp
using IO.Swagger.Api;
using IO.Swagger.Client;
using Model;
```

## Getting Started

```csharp
using System;
using System.Diagnostics;
using IO.Swagger.Api;
using IO.Swagger.Client;
using Model;

namespace Example
{
    public class Example
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

<a name="documentation-for-api-endpoints"></a>
## Documentation for API Endpoints

All URIs are relative to *https://www.waitlisted.co/api/v2*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*ReservationApi* | [**ActivateReservation**](docs/ReservationApi.md#activatereservation) | **POST** /reservations/activate | 
*ReservationApi* | [**CreateReservation**](docs/ReservationApi.md#createreservation) | **POST** /reservations | 
*ReservationApi* | [**DeleteReservation**](docs/ReservationApi.md#deletereservation) | **DELETE** /reservations | 
*ReservationApi* | [**GetReservation**](docs/ReservationApi.md#getreservation) | **GET** /reservations | 
*SiteApi* | [**GetSite**](docs/SiteApi.md#getsite) | **GET** /site | 


<a name="documentation-for-models"></a>
## Documentation for Models

 - [Model.ErrorResponse](docs/ErrorResponse.md)
 - [Model.FormResponse](docs/FormResponse.md)
 - [Model.Reservation](docs/Reservation.md)
 - [Model.ReservationRequest](docs/ReservationRequest.md)
 - [Model.ReservationsResponse](docs/ReservationsResponse.md)
 - [Model.SiteResponse](docs/SiteResponse.md)


## Documentation for Authorization

### api_key

- **Type**: API key
- **API key parameter name**: X-API-Key
- **Location**: HTTP header

