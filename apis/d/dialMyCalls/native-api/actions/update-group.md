# Update Group with DialMyCalls

Updates an existing group in DialMyCalls.

## Endpoint

- **Method:** `PUT`
- **Path:** `/group/:GroupId`
- **Base URL:** `https://{apiKey}@api.dialmycalls.com/2.0`
- **Official documentation:** [Update Group](https://www.dialmycalls.com/api-documentation#group-update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `GroupId` | path | `string` | yes | The DialMyCalls group ID to update. |
| `name` | body | `string` | yes | The contact group's name. |
