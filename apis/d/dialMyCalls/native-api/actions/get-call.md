# Get Call with DialMyCalls

Retrieves a call from DialMyCalls.

## Endpoint

- **Method:** `GET`
- **Path:** `/service/call/:CallId`
- **Base URL:** `https://{apiKey}@api.dialmycalls.com/2.0`
- **Official documentation:** [Get Call](https://www.dialmycalls.com/api-documentation#call-get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `CallId` | path | `string` | yes | The DialMyCalls call ID to retrieve. |
