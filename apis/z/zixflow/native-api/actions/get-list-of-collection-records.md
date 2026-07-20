# Get List of Collection Records with Zixflow

Retrieves collection records from Zixflow.

## Endpoint

- **Method:** `POST`
- **Path:** `/collection-records/:collectionId/query`
- **Base URL:** `https://api.zixflow.com/api/v1`
- **Official documentation:** [Get List of Collection Records](https://docs.zixflow.com/api-reference/records/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `collectionId` | path | `string` | yes | Collection identifier. |
| `filter` | body | `object` | no | Filter object for collection-record query. |
| `sort[]` | body | `array` | no | Sort instructions for collection-record query. |
| `limit` | body | `number` | no | Maximum number of records to return. |
| `offset` | body | `number` | no | Number of records to skip. |
