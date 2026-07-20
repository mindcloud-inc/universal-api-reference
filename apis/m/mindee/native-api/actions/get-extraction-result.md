# Get Extraction Result with Mindee

Retrieves an extraction result from Mindee.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/products/extraction/results/:inference_id`
- **Base URL:** `https://api-v2.mindee.net`
- **Official documentation:** [Get Extraction Result](https://docs.mindee.com/integrations/api-reference/extraction-models)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `inference_id` | path | `string` | yes | UUID of the inference to retrieve. |
