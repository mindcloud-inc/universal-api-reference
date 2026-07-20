# Get Index Stats with Pinecone

Retrieves statistics for a Pinecone index.

## Endpoint

- **Method:** `POST`
- **Path:** `{indexHost}/describe_index_stats`
- **Base URL:** `https://api.pinecone.io`
- **Official documentation:** [Get Index Stats](https://docs.pinecone.io/reference/api/2025-10/data-plane/describeindexstats)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filter` | body | `object` | no | A metadata filter to limit returned stats on supported indexes. |
