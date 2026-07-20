# Add Feedback Tags with Retently

Updates tags on a feedback response in Retently.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/response/tags`
- **Base URL:** `https://app.retently.com`
- **Official documentation:** [Add Feedback Tags](https://www.retently.com/api/#api-add-response-tags-post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `string` | yes | Response ID; |
| `tags[]` | body | `array<string>` | no | An array of tags; |
| `op` | body | `string` | no | Use the flag âappendâ in order to append the tags to the response, or leave it empty in order to override existing tags; |
