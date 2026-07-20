# Create Sequence with AI with Sequenzy

Creates an AI-generated sequence in Sequenzy.

## Endpoint

- **Method:** `POST`
- **Path:** `/sequences`
- **Base URL:** `https://api.sequenzy.com/api/v1`
- **Official documentation:** [Create Sequence with AI](https://docs.sequenzy.com/api-reference/sequences/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `eventName` | body | `string` | yes | Trigger event name. |
| `goal` | body | `string` | no | What the sequence should accomplish. |
| `name` | body | `string` | yes | Sequence name. |
