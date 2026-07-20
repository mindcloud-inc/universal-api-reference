# Get Summary with LunaNotes

Retrieves a summary from LunaNotes.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/summaries/:id`
- **Base URL:** `https://api.lunanotes.io`
- **Official documentation:** [Get Summary](https://lunanotes.io/docs/summaries/get-v1-summaries-id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The LunaNotes summary ID. |
| `include` | query | `string` | no | Include related video, transcript, or FAQs in the response |
