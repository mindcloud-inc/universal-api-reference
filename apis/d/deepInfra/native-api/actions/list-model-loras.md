# List Model LoRAs with Deep Infra

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/model/:model_name/loras`
- **Base URL:** `https://api.deepinfra.com`
- **Official documentation:** [List Model LoRAs](https://docs.deepinfra.com/api-reference/lora-adapters/get-model-loras)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `model_name` | path | `string` | yes | DeepInfra model identifier whose LoRA adapters should be listed. |
