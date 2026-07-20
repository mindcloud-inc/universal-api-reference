# Pachca (Admin): List Messages

Retrieves messages from the Pachca Admin API.

```
GET https://connect.mindcloud.co/v1/universal/pachcaAdmin/latest/actions/list-messages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pachca (Admin) `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pachcaAdmin/latest/actions/list-messages?connectionId=$CONNECTION_ID&chatId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "chatId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pachcaAdmin/latest/actions/list-messages?${params}`, {
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
| `chatId` | number | yes |  |
| `order` | string | no | Sort direction. |
| `sort` | string | no | Sort direction hint from provider docs. |
| `limit` | number | no |  |
| `cursor` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {
          "buttons": {},
          "changedAt": "string",
          "chatId": 1,
          "content": "string",
          "createdAt": "string",
          "deletedAt": {},
          "entityId": 1,
          "entityType": "string",
          "forwarding": {},
          "id": 1,
          "parentMessageId": {},
          "rootChatId": 1,
          "thread": {},
          "url": "https://example.com",
          "userId": 1
        }
      ],
      "meta": {
        "paginate": {
          "nextPage": "string"
        }
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data[].buttons` | object |  |
| `data[].changedAt` | string |  |
| `data[].chatId` | number |  |
| `data[].content` | string |  |
| `data[].createdAt` | string |  |
| `data[].deletedAt` | object |  |
| `data[].entityId` | number |  |
| `data[].entityType` | string |  |
| `data[].forwarding` | object |  |
| `data[].id` | number |  |
| `data[].parentMessageId` | object |  |
| `data[].rootChatId` | number |  |
| `data[].thread` | object |  |
| `data[].url` | string |  |
| `data[].userId` | number |  |
| `meta.paginate.nextPage` | string |  |

## Native endpoint

Through the native Pachca (Admin) API, this operation is `GET /messages` (base URL `https://api.pachca.com/api/shared/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-messages.md) for the provider-specific parameters and requirements.

