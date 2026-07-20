# Update Instruction with Koncile OCR

## Endpoint

- **Method:** `PUT`
- **Path:** `/update_instruction`
- **Base URL:** `https://api.koncile.ai/v1`
- **Official documentation:** [Update Instruction](https://docs.koncile.ai/api-setup/instructions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `content` | body | `string` | no | Update the instruction text. |
| `instruction_id` | query | `number` | yes | The instruction identifier to update. |
| `type` | body | `string` | no | Update whether the instruction targets General fields or Line fields. |
