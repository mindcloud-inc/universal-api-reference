# Livestorm: List Session Questions

Retrieves questions for a session from Livestorm.

```
GET https://connect.mindcloud.co/v1/universal/livestorm/latest/actions/list-session-questions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Livestorm `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/livestorm/latest/actions/list-session-questions?connectionId=$CONNECTION_ID&limit=25&offset=0&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/livestorm/latest/actions/list-session-questions?${params}`, {
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
| `id` | string | yes | Session ID |
| `include` | string | no | Include Related Data Accepts multiple values in one string, delimited by `,`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {
        "createdAt": 1,
        "eventId": "string",
        "question": "string",
        "respondedAt": 1,
        "response": "string",
        "responseOrally": true,
        "sessionId": "string",
        "updatedAt": 1
      },
      "id": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes.createdAt` | number |  |
| `attributes.eventId` | string |  |
| `attributes.question` | string |  |
| `attributes.respondedAt` | number |  |
| `attributes.response` | string |  |
| `attributes.responseOrally` | boolean |  |
| `attributes.sessionId` | string |  |
| `attributes.updatedAt` | number |  |
| `id` | string | ID |
| `type` | string | Type |

## Native endpoint

Through the native Livestorm API, this operation is `GET sessions/:id/questions` (base URL `https://api.livestorm.co/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-session-questions.md) for the provider-specific parameters and requirements.

