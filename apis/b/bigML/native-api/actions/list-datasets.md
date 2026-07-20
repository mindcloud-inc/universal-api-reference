# List Datasets with BigML

Retrieves datasets from BigML.

## Endpoint

- **Method:** `GET`
- **Path:** `/dataset`
- **Base URL:** `https://bigml.io`
- **Official documentation:** [List Datasets](https://bigml.com/api/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `number` | no | Maximum number of datasets to return. |
| `offset` | query | `number` | no | Pagination offset for dataset listing. |
