# SWGPassApi

All URIs are relative to *https://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**createOrUpdatePass**](SWGPassApi.md#createorupdatepass) | **POST** /pass | This method creates or (if the pass id already exists) updates a pass, so you don&#39;t have to track ids and creation status of your passes.
[**deletePass**](SWGPassApi.md#deletepass) | **DELETE** /pass | Delete pass by pass id.
[**getPass**](SWGPassApi.md#getpass) | **GET** /pass | Get pass information by pass id.
[**passList**](SWGPassApi.md#passlist) | **GET** /pass/list | Retrieve the list of active pass ids for a given pass type.
[**passSync**](SWGPassApi.md#passsync) | **POST** /pass/sync | Send updates to all active passes for a given pass type.


# **createOrUpdatePass**
```objc
-(NSURLSessionTask*) createOrUpdatePassWithPassTypeId: (NSObject*) passTypeId
    passId: (NSObject*) passId
        completionHandler: (void (^)(NSError* error)) handler;
```

This method creates or (if the pass id already exists) updates a pass, so you don't have to track ids and creation status of your passes.

This method creates or (if the pass id already exists) updates a pass, so you don't have to track ids and creation status of your passes.

### Example 
```objc

NSObject* passTypeId = [[NSObject alloc] init]; // your pass type id, for example P963493 (Urban Fitness)
NSObject* passId = [[NSObject alloc] init]; // id of the pass (provided by you when creating the pass or automatically set by passmeister) (optional)

SWGPassApi*apiInstance = [[SWGPassApi alloc] init];

// This method creates or (if the pass id already exists) updates a pass, so you don't have to track ids and creation status of your passes.
[apiInstance createOrUpdatePassWithPassTypeId:passTypeId
              passId:passId
          completionHandler: ^(NSError* error) {
                        if (error) {
                            NSLog(@"Error calling SWGPassApi->createOrUpdatePass: %@", error);
                        }
                    }];
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **passTypeId** | [**NSObject***](.md)| your pass type id, for example P963493 (Urban Fitness) | 
 **passId** | [**NSObject***](.md)| id of the pass (provided by you when creating the pass or automatically set by passmeister) | [optional] 

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **deletePass**
```objc
-(NSURLSessionTask*) deletePassWithPassTypeId: (NSObject*) passTypeId
    passId: (NSObject*) passId
        completionHandler: (void (^)(NSError* error)) handler;
```

Delete pass by pass id.

Delete pass by pass id.

### Example 
```objc

NSObject* passTypeId = [[NSObject alloc] init]; // your pass type id, for example P963493 (Urban Fitness)
NSObject* passId = [[NSObject alloc] init]; // id of the pass

SWGPassApi*apiInstance = [[SWGPassApi alloc] init];

// Delete pass by pass id.
[apiInstance deletePassWithPassTypeId:passTypeId
              passId:passId
          completionHandler: ^(NSError* error) {
                        if (error) {
                            NSLog(@"Error calling SWGPassApi->deletePass: %@", error);
                        }
                    }];
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **passTypeId** | [**NSObject***](.md)| your pass type id, for example P963493 (Urban Fitness) | 
 **passId** | [**NSObject***](.md)| id of the pass | 

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getPass**
```objc
-(NSURLSessionTask*) getPassWithPassTypeId: (NSObject*) passTypeId
    passId: (NSObject*) passId
        completionHandler: (void (^)(NSError* error)) handler;
```

Get pass information by pass id.

Get pass information by pass id.

### Example 
```objc

NSObject* passTypeId = [[NSObject alloc] init]; // your pass type id, for example P963493 (Urban Fitness)
NSObject* passId = [[NSObject alloc] init]; // id of the pass

SWGPassApi*apiInstance = [[SWGPassApi alloc] init];

// Get pass information by pass id.
[apiInstance getPassWithPassTypeId:passTypeId
              passId:passId
          completionHandler: ^(NSError* error) {
                        if (error) {
                            NSLog(@"Error calling SWGPassApi->getPass: %@", error);
                        }
                    }];
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **passTypeId** | [**NSObject***](.md)| your pass type id, for example P963493 (Urban Fitness) | 
 **passId** | [**NSObject***](.md)| id of the pass | 

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **passList**
```objc
-(NSURLSessionTask*) passListWithPassTypeId: (NSObject*) passTypeId
    page: (NSObject*) page
    limit: (NSObject*) limit
        completionHandler: (void (^)(NSError* error)) handler;
```

Retrieve the list of active pass ids for a given pass type.

Retrieve the list of active pass ids for a given pass type.

### Example 
```objc

NSObject* passTypeId = [[NSObject alloc] init]; // your pass type id, for example P963493 (Urban Fitness)
NSObject* page = [[NSObject alloc] init]; //  (optional)
NSObject* limit = [[NSObject alloc] init]; //  (optional)

SWGPassApi*apiInstance = [[SWGPassApi alloc] init];

// Retrieve the list of active pass ids for a given pass type.
[apiInstance passListWithPassTypeId:passTypeId
              page:page
              limit:limit
          completionHandler: ^(NSError* error) {
                        if (error) {
                            NSLog(@"Error calling SWGPassApi->passList: %@", error);
                        }
                    }];
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **passTypeId** | [**NSObject***](.md)| your pass type id, for example P963493 (Urban Fitness) | 
 **page** | [**NSObject***](.md)|  | [optional] 
 **limit** | [**NSObject***](.md)|  | [optional] 

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **passSync**
```objc
-(NSURLSessionTask*) passSyncWithPassTypeId: (NSObject*) passTypeId
        completionHandler: (void (^)(NSError* error)) handler;
```

Send updates to all active passes for a given pass type.

For example: you changed the pass type layout and now you want to update all installed passes. (The API call only confirms the scheduling of the updates, actual updating of passes on your customers devices can take a while.)

### Example 
```objc

NSObject* passTypeId = [[NSObject alloc] init]; // your pass type id, for example P963493 (Urban Fitness)

SWGPassApi*apiInstance = [[SWGPassApi alloc] init];

// Send updates to all active passes for a given pass type.
[apiInstance passSyncWithPassTypeId:passTypeId
          completionHandler: ^(NSError* error) {
                        if (error) {
                            NSLog(@"Error calling SWGPassApi->passSync: %@", error);
                        }
                    }];
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **passTypeId** | [**NSObject***](.md)| your pass type id, for example P963493 (Urban Fitness) | 

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

