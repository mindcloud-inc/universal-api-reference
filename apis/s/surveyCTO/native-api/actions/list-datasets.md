# List Datasets with SurveyCTO

Retrieves all available datasets from SurveyCTO.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/datasets`
- **Base URL:** `https://mindcloudsurvey.surveycto.com/api`
- **Official documentation:** [List Datasets](https://developer.surveycto.com/api-v2.html#getDatasets)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `teamId` | query | `string` | no | Filter datasets by team ID. |
