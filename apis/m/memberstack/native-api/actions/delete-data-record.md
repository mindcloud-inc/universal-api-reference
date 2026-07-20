# Delete Data Record with Memberstack

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v2/data-tables/:tableKey/records/:recordId`
- **Base URL:** `https://admin.memberstack.com`
- **Official documentation:** [Delete Data Record](https://developers.memberstack.com/admin-rest-api/data-tables)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tableKey` | path | `string` | yes | Target data table key. |
| `recordId` | path | `string` | yes | Record identifier to delete from the data table. |
