# Create Modeling Request with Modelry

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/modeling-requests`
- **Base URL:** `https://api.modelry.ai/api`
- **Official documentation:** [Create Modeling Request](https://files.cgtarsenal.com/api/doc/index.html#api-ModelingRequests-CreateModelingRequest)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `modeling_request.title` | body | `string` | yes | Modeling request title. |
| `modeling_request.sku` | body | `string` | yes | Modeling request SKU. |
| `modeling_request.product_id` | body | `number` | yes | Associated product ID. |
| `modeling_request.dimensions` | body | `string` | yes | Dimensions string. |
| `modeling_request.pipeline` | body | `string` | yes | Pipeline, such as high_poly or low_poly. |
| `modeling_request.specific_requirements` | body | `string` | yes | Specific modeling requirements. |
| `modeling_request.external_url` | body | `string` | yes | External URL for the request. |
| `modeling_request.reference_file_blob_ids[]` | body | `array<string>` | yes | Signed blob IDs from uploads. |
