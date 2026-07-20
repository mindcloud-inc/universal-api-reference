# Create Block with Letta

Creates a new block in Letta.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/blocks/`
- **Base URL:** `https://api.letta.com`
- **Official documentation:** [Create Block](https://docs.letta.com/api/resources/blocks/methods/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `label` | body | `string` | yes | The memory block label. |
| `value` | body | `string` | yes | The memory block value. |
