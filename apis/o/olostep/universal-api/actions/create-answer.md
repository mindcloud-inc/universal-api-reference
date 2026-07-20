# Olostep: Create Answer

Creates a new answer in Olostep.

```
POST https://connect.mindcloud.co/v1/universal/olostep/latest/actions/create-answer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Olostep `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/olostep/latest/actions/create-answer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "task": "Summarize the pricing information on https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/olostep/latest/actions/create-answer', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "task": "Summarize the pricing information on https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `task` | string | yes | The question or task Olostep should answer. Example: `Summarize the pricing information on https://example.com`. |

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
        "jsonHostedUrl": "https://example.com",
        "sources": [
          "string"
        ]
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
| `result.sources[]` | string |  |
| `task` | string |  |

## Native endpoint

Through the native Olostep API, this operation is `POST /v1/answers` (base URL `https://api.olostep.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-answer.md) for the provider-specific parameters and requirements.

