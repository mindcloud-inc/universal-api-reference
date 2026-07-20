# Create Instruction with Koncile OCR

## Endpoint

- **Method:** `POST`
- **Path:** `/create_instruction`
- **Base URL:** `https://api.koncile.ai/v1`
- **Official documentation:** [Create Instruction](https://docs.koncile.ai/api-setup/instructions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `content` | body | `string` | yes | The instruction text. |
| `template_id` | body | `string` | yes | The template identifier the instruction belongs to. |
| `type` | body | `string` | yes | Whether the instruction targets General fields or Line fields. |
