# Get Split Result with Mindee

Retrieves a split result from Mindee.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/products/split/results/:inference_id`
- **Base URL:** `https://api-v2.mindee.net`
- **Official documentation:** [Get Split Result](https://docs.mindee.com/integrations/api-reference/split-models)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `inference_id` | path | `string` | yes | UUID of the inference to retrieve. |
