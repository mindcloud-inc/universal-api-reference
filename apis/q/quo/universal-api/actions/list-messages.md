# Quo: List Messages

Retrieves all messages from Quo.

```
GET https://connect.mindcloud.co/v1/universal/quo/latest/actions/list-messages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Quo `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/quo/latest/actions/list-messages?connectionId=$CONNECTION_ID&limit=25&offset=0&participants%5B%5D=string&phoneNumberId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "participants[]": "string",
  "phoneNumberId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/quo/latest/actions/list-messages?${params}`, {
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
| `createdAfter` | date | no |  |
| `createdBefore` | date | no |  |
| `participants[]` | array<string> | yes |  |
| `phoneNumberId` | string | yes |  |
| `userId` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "direction": "string",
      "from": "string",
      "id": "string",
      "phoneNumberId": "string",
      "status": "string",
      "text": "string",
      "to": [
        "string"
      ],
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "userId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `direction` | string |  |
| `from` | string |  |
| `id` | string |  |
| `phoneNumberId` | string |  |
| `status` | string |  |
| `text` | string |  |
| `to` | array<string> |  |
| `updatedAt` | date |  |
| `userId` | string |  |

## Native endpoint

Through the native Quo API, this operation is `GET /messages` (base URL `https://api.openphone.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-messages.md) for the provider-specific parameters and requirements.

