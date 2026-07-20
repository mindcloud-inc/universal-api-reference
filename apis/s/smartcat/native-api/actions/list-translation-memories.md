# List Translation Memories with Smartcat

Retrieves translation memories from the current Smartcat account.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/integration/v1/translationmemory`
- **Base URL:** `https://smartcat.ai`
- **Official documentation:** [List Translation Memories](https://developers.smartcat.com/api/#fetch-the-available-tms-filtered-per-account)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `batchSize` | query | `number` | yes | Number of translation memories to return |
