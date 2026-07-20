# Update User API Key with BlazeMeter

## Endpoint

- **Method:** `PUT`
- **Path:** `/user/api-keys/:apiKeyId`
- **Base URL:** `https:///a.blazemeter.com/api/v4`
- **Official documentation:** [Update User API Key](https://help.blazemeter.com/apidocs/#tag/user/operation/apiKeysUpdateApiKey)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `apiKeyId` | path | `string` | yes |
| `name` | body | `string` | yes |
