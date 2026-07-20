# Create Sequence with Storyscale

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/sequence/create`
- **Base URL:** `https://prodapi.storyscale.com/api`
- **Official documentation:** [Create Sequence](https://prodapi.storyscale.com/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `active` | body | `boolean` | no | Whether the sequence is active. |
| `language_id` | body | `number` | no | Language for the sequence. |
| `marketing_persona_id` | body | `number` | no | Marketing persona for the sequence. |
| `marketing_segment_id` | body | `number` | no | Marketing segment for the sequence. |
| `published` | body | `boolean` | no | Whether the sequence is published. |
| `sequence_name` | body | `string` | no | Name for the new sequence. |
