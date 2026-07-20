# Delete Group with DialMyCalls

Deletes an existing group from DialMyCalls.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/group/:GroupId`
- **Base URL:** `https://{apiKey}@api.dialmycalls.com/2.0`
- **Official documentation:** [Delete Group](https://www.dialmycalls.com/api-documentation#group-delete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `GroupId` | path | `string` | yes | The DialMyCalls group ID to delete. |
