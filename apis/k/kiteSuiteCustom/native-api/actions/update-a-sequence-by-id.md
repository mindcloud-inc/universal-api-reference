# Update a sequence by ID with Kite Suite

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v1/campaign/sequence/:id`
- **Base URL:** `https://api.kitesuite.com`
- **Official documentation:** [Update a sequence by ID](https://api.kitesuite.com/swagger/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The ID of the sequence to update. |
| `body` | body | `object` | yes | Request body |
| `subject` | body | `string` | yes | The subject of the sequence. |
| `nextMessage` | body | `string` | yes | The next message in the sequence (if any). |
| `attachments[]` | body | `array` | yes | List of attachment URLs or IDs. |
