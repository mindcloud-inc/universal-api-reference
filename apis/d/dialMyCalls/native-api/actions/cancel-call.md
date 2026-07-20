# Cancel Call with DialMyCalls

Cancels an existing call in DialMyCalls.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/service/call/:CallId`
- **Base URL:** `https://{apiKey}@api.dialmycalls.com/2.0`
- **Official documentation:** [Cancel Call](https://www.dialmycalls.com/api-documentation#call-cancel)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `CallId` | path | `string` | yes | The DialMyCalls call broadcast to cancel. |
