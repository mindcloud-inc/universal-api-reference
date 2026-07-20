# Delete API Key with Snappy

Deletes an existing API key from Snappy.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/authentication/apiKeys/{apiKeyId}`
- **Base URL:** `https://api.snappy.com/public-api/v2`
- **Official documentation:** [Delete API Key](https://docs.snappy.com/reference/deleteapikey)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `apiKeyId` | path | `string` | yes | The API key id. |
| `companyId` | query | `string` | no | Company ID. |
