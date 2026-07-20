# Get Model Schema with Deep Infra

## Endpoint

- **Method:** `GET`
- **Path:** `/models/:model_name/schema/:variantKey`
- **Base URL:** `https://api.deepinfra.com`
- **Official documentation:** [Get Model Schema](https://docs.deepinfra.com/api-reference/models/model-schema)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `model_name` | path | `string` | yes | DeepInfra model identifier from the model URL path. |
| `variantKey` | path | `string` | yes | Schema variant key from the model schema URL path. |
