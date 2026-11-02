# Get Fields from Dataset V1 2 with BambooHR

Retrieves fields from dataset v1 2 from BambooHR.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1_2/datasets/:datasetName/fields`
- **Base URL:** `https://{companyDomain}.bamboohr.com/api`
- **Official documentation:** [Get Fields from Dataset V1 2](https://documentation.bamboohr.com/reference/get-fields-from-dataset-v1_2)

## Requirements

- **OAuth scopes:** `report`
- **scope:** `report` — BambooHR documents these OAuth scopes for this endpoint; access also follows the connected user permissions.

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `datasetName` | path | `string` | yes | The name of the dataset to retrieve fields for. Use "List Datasets (v1.2)" to discover valid names. |
