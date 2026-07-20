# Create a new sequence with Kite Suite

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/campaign/sequence`
- **Base URL:** `https://api.kitesuite.com`
- **Official documentation:** [Create a new sequence](https://api.kitesuite.com/swagger/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `body` | body | `object` | yes | Request body |
| `subject` | body | `string` | yes | The subject of the sequence. |
| `campaign` | body | `string` | yes | The ID of the campaign to associate the sequence with. |
| `nextMessage` | body | `string` | yes | The next message in the sequence (if any). |
