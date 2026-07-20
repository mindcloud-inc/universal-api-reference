# Update Caller ID with DialMyCalls

Updates an existing caller ID in DialMyCalls.

## Endpoint

- **Method:** `PUT`
- **Path:** `/callerid/:CalleridId`
- **Base URL:** `https://{apiKey}@api.dialmycalls.com/2.0`
- **Official documentation:** [Update Caller ID](https://www.dialmycalls.com/api-documentation#callerid-update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `CalleridId` | path | `string` | yes | The DialMyCalls caller ID to update. |
| `name` | body | `string` | yes | The caller ID's name. |
