# Quo: Get Message By ID

Retrieves a message from Quo by ID.

```
GET https://connect.mindcloud.co/v1/universal/quo/latest/actions/get-message-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Quo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/quo/latest/actions/get-message-by-id?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/quo/latest/actions/get-message-by-id?${params}`, {
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
| `id` | string | yes |  |

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

Through the native Quo API, this operation is `GET /messages/:id` (base URL `https://api.openphone.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-message-by-id.md) for the provider-specific parameters and requirements.

