# List Datasets with Apify

Retrieves datasets from Apify.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/datasets`
- **Base URL:** `https://api.apify.com`
- **Official documentation:** [List Datasets](https://docs.apify.com/api/v2/datasets-get)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ownership` | query | `string` | no | Filter datasets by ownership: ownedByMe or sharedWithMe. |
