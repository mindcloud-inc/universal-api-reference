# Cancel Text with DialMyCalls

Cancels an existing text in DialMyCalls.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/service/text/:TextId`
- **Base URL:** `https://{apiKey}@api.dialmycalls.com/2.0`
- **Official documentation:** [Cancel Text](https://www.dialmycalls.com/api-documentation#text-cancel)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `TextId` | path | `string` | yes | The DialMyCalls text broadcast to cancel. |
