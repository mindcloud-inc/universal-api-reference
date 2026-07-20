# Create Data Record with Memberstack

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/data-tables/:tableKey/records`
- **Base URL:** `https://admin.memberstack.com`
- **Official documentation:** [Create Data Record](https://developers.memberstack.com/admin-rest-api/data-tables)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tableKey` | path | `string` | yes | Target data table key. |
| `data` | body | `object` | yes | Record payload object to create in the table. |
