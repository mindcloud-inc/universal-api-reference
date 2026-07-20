# Missive: List Conversation Messages

Retrieves messages from a Missive conversation.

```
GET https://connect.mindcloud.co/v1/universal/missive/latest/actions/list-conversation-messages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Missive `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/missive/latest/actions/list-conversation-messages?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/missive/latest/actions/list-conversation-messages?${params}`, {
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
| `id` | string | yes | Conversation ID. |
| `limit` | number | no | Number of messages returned. Default and max 10. |
| `until` | number | no | Unix timestamp used to paginate with the oldest message delivered_at value from the previous page. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "author": {},
      "createdAt": 1,
      "deliveredAt": 1,
      "externalId": {},
      "fromField": {
        "id": "string",
        "name": "Ava Chen",
        "username": "Ava Chen"
      },
      "id": "string",
      "preview": "string",
      "toFields": [
        {
          "id": "string",
          "name": "Ava Chen",
          "username": "Ava Chen"
        }
      ],
      "type": "string",
      "updatedAt": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `author` | object |  |
| `createdAt` | number |  |
| `deliveredAt` | number |  |
| `externalId` | object |  |
| `fromField.id` | string |  |
| `fromField.name` | string |  |
| `fromField.username` | string |  |
| `id` | string |  |
| `preview` | string |  |
| `toFields[].id` | string |  |
| `toFields[].name` | string |  |
| `toFields[].username` | string |  |
| `type` | string |  |
| `updatedAt` | number |  |

## Native endpoint

Through the native Missive API, this operation is `GET /conversations/:id/messages` (base URL `https://public.missiveapp.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-conversation-messages.md) for the provider-specific parameters and requirements.

