# Get Webhook Example Data with Placker

## Endpoint

- **Method:** `GET`
- **Path:** `/webhook/:board/example`
- **Base URL:** `https://api.placker.com`
- **Official documentation:** [Get Webhook Example Data](https://placker.com/docs/api/paths/webhook.yaml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `board` | path | `number` | yes | Board ID. |
| `events[]` | query | `array<string>` | yes | Event types to get example data for. |
