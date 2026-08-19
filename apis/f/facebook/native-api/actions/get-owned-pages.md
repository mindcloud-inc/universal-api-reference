# Get Owned Pages with Facebook

Retrieve a list of Pages owned by the specified business account.

## Endpoint

- **Method:** `GET`
- **Path:** `:businessId/owned_pages?fields=id,name,access_token`
- **Base URL:** `https://graph.facebook.com/v25.0`

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `businessId` | path | `string` | yes |
