# Get Classification Result with Mindee

Retrieves a classification result from Mindee.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/products/classification/results/:inference_id`
- **Base URL:** `https://api-v2.mindee.net`
- **Official documentation:** [Get Classification Result](https://docs.mindee.com/integrations/api-reference/classification-models)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `inference_id` | path | `string` | yes | UUID of the inference to retrieve. |
