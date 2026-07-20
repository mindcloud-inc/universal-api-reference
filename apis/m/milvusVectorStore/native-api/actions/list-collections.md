# List Collections with Milvus Vector Store

Retrieves collections from Milvus Vector Store.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/vectordb/collections/list`
- **Base URL:** `https://{clusterEndpoint}`
- **Official documentation:** [List Collections](https://docs.zilliz.com/reference/restful/list-collections-v2)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `dbName` | body | `string` | no | Database name that owns the collections to list. |
