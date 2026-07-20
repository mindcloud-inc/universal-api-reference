# Update Data Record with Memberstack

## Endpoint

- **Method:** `PUT`
- **Path:** `/v2/data-tables/:tableKey/records/:recordId`
- **Base URL:** `https://admin.memberstack.com`
- **Official documentation:** [Update Data Record](https://developers.memberstack.com/admin-rest-api/data-tables)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tableKey` | path | `string` | yes | Target data table key. |
| `recordId` | path | `string` | yes | Record identifier within the data table. |
| `data` | body | `object` | yes | Updated record payload object. |
