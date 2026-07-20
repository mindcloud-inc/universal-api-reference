# Get Dataset Items with Apify

Retrieves items from an Apify dataset.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/datasets/:datasetId/items`
- **Base URL:** `https://api.apify.com`
- **Official documentation:** [Get Dataset Items](https://docs.apify.com/api/v2/dataset-items-get)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `datasetId` | path | `string` | yes | The ID of the dataset whose items to retrieve. |
