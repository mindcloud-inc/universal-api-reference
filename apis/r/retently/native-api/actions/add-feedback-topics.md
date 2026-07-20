# Add Feedback Topics with Retently

Updates topics on a feedback response in Retently.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/response/topics`
- **Base URL:** `https://app.retently.com`
- **Official documentation:** [Add Feedback Topics](https://www.retently.com/api/#api-add-response-topics-post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `string` | yes | Response ID; |
| `topics[]` | body | `array<object>` | no | An array of topic objects |
| `topics[].name` | body | `string` | yes | The topic name |
| `topics[].sentiment` | body | `string` | no | The sentiment of the topic (if not provided, defaults to 'neutral') |
| `op` | body | `string` | no | Use the flag âappendâ in order to append the topics to the response, or leave it empty in order to override existing topics assigned to the response; |
