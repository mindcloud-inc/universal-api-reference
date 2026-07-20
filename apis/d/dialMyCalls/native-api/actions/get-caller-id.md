# Get Caller ID with DialMyCalls

Retrieves a caller ID from DialMyCalls.

## Endpoint

- **Method:** `GET`
- **Path:** `/callerid/:CalleridId`
- **Base URL:** `https://{apiKey}@api.dialmycalls.com/2.0`
- **Official documentation:** [Get Caller ID](https://www.dialmycalls.com/api-documentation#callerid-get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `CalleridId` | path | `string` | yes | The DialMyCalls caller ID to retrieve. |
