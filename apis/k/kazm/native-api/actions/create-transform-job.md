# Create Transform Job with Kazm

Creates a transform job in Kazm.

## Endpoint

- **Method:** `POST`
- **Path:** `/transform-jobs`
- **Base URL:** `https://api.lightningrod.ai/api/public/v1`
- **Official documentation:** [Create Transform Job](https://docs.lightningrod.ai/rest-api/transform-jobs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `config` | body | `object` | yes | Transform job configuration payload. |
| `inputDatasetId` | body | `string` | no | Dataset ID to use as the input dataset. |
