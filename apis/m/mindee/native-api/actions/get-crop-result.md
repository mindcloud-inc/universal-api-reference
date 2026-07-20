# Get Crop Result with Mindee

Retrieves a crop result from Mindee.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/products/crop/results/:inference_id`
- **Base URL:** `https://api-v2.mindee.net`
- **Official documentation:** [Get Crop Result](https://docs.mindee.com/integrations/api-reference/crop-models)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `inference_id` | path | `string` | yes | UUID of the inference to retrieve. |
