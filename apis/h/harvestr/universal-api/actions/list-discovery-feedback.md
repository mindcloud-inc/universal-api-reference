# Harvestr.io: List Discovery Feedback



```
GET https://connect.mindcloud.co/v1/universal/harvestr/latest/actions/list-discovery-feedback
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Harvestr.io `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/harvestr/latest/actions/list-discovery-feedback?connectionId=$CONNECTION_ID&limit=25&offset=0&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/harvestr/latest/actions/list-discovery-feedback?${params}`, {
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
| `id` | string | yes | Unique identifier (id or clientId) |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `createdBefore` | date | no | Filter items created before this date (ISO 8601 format) |
| `createdAfter` | date | no | Filter items created after this date (ISO 8601 format) |
| `updatedBefore` | date | no | Filter items updated before this date (ISO 8601 format) |
| `updatedAfter` | date | no | Filter items updated after this date (ISO 8601 format) |
| `messageId` | string | no | Filter feedback by message ID |

## Response

```json
{
  "success": true,
  "data": [
    {
      "clientId": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "discoveryId": "string",
      "id": "string",
      "messageId": "string",
      "score": 1,
      "selections": {
        "clientId": "string",
        "content": "string",
        "createdAt": "2026-05-07T12:00:00.000Z",
        "fullSelection": true,
        "id": "string",
        "updatedAt": "2026-05-07T12:00:00.000Z"
      },
      "starred": true,
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `clientId` | string | Client identifier |
| `createdAt` | date | Creation date of the feedback |
| `discoveryId` | string | Identifier of the associated discovery |
| `id` | string | Unique identifier of the feedback |
| `messageId` | string | Identifier of the associated message |
| `score` | number | Score associated with the feedback |
| `selections` | array<object> | List of selections within the feedback |
| `selections.clientId` | string | Client identifier |
| `selections.content` | string | Text content of the selection |
| `selections.createdAt` | date | Creation date of the selection |
| `selections.fullSelection` | boolean | Whether this selection covers the full feedback content |
| `selections.id` | string | Unique identifier of the selection |
| `selections.updatedAt` | date | Last update date of the selection |
| `starred` | boolean | Whether the feedback is starred |
| `updatedAt` | date | Last update date of the feedback |

## Native endpoint

Through the native Harvestr.io API, this operation is `GET /discovery/{id}/feedback` (base URL `https://rest.harvestr.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-discovery-feedback.md) for the provider-specific parameters and requirements.

