# Olostep: Get Answer

Retrieves details for an answer in Olostep.

```
GET https://connect.mindcloud.co/v1/universal/olostep/latest/actions/get-answer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Olostep `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/olostep/latest/actions/get-answer?connectionId=$CONNECTION_ID&answerId=answer_123" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "answerId": "answer_123"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/olostep/latest/actions/get-answer?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `answerId` | string | yes | The ID of the answer to retrieve. Example: `answer_123`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "object": "string",
      "result": {
        "jsonContent": "string",
        "jsonHostedUrl": "https://example.com"
      },
      "task": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | date |  |
| `id` | string |  |
| `object` | string |  |
| `result.jsonContent` | string |  |
| `result.jsonHostedUrl` | string |  |
| `task` | string |  |

## Native endpoint

Through the native Olostep API, this operation is `GET /v1/answers/[:answer_id]` (base URL `https://api.olostep.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-answer.md) for the provider-specific parameters and requirements.

