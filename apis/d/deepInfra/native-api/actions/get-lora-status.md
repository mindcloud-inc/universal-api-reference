# Get LoRA Status with Deep Infra

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/lora/:lora_name/status`
- **Base URL:** `https://api.deepinfra.com`
- **Official documentation:** [Get LoRA Status](https://docs.deepinfra.com/api-reference/lora-adapters/get-lora-status)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `lora_name` | path | `string` | yes | LoRA adapter name from the LoRA status URL path. |
