# lemlist: List Inboxes

Retrieves your inbox conversations from lemlist.

```
GET https://connect.mindcloud.co/v1/universal/lemlist/latest/actions/list-inboxes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a lemlist `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lemlist/latest/actions/list-inboxes?connectionId=$CONNECTION_ID&userId=usr_vvv9vehz2Ghvgbedv" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "userId": "usr_vvv9vehz2Ghvgbedv"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lemlist/latest/actions/list-inboxes?${params}`, {
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
| `userId` | string | yes | Filter by user ID. Example: `usr_vvv9vehz2Ghvgbedv`. |
| `page` | number | no | Page number to retrieve. Example: `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {
          "channels": [
            "string"
          ],
          "contact": {
            "email": "ava@example.com",
            "fullName": "Ava Chen",
            "id": "string"
          },
          "contactId": "string",
          "createdAt": "string",
          "createdBy": "string",
          "haveReplies": true,
          "id": "string",
          "isYourTurn": true,
          "lastActivityAt": "string",
          "lastRepliedAt": "string",
          "lastRepliedChannel": "string",
          "lastRepliedSubject": "string",
          "lastSentAt": "string",
          "lastSentMessagePreview": "string",
          "lastSentSubject": "string",
          "opportunities": [
            "string"
          ],
          "teamId": "string",
          "users": [
            {
              "read": true,
              "sender": true,
              "userId": "string"
            }
          ]
        }
      ],
      "pagination": {
        "currentPage": 1,
        "nextPage": "string",
        "perPage": 1,
        "previousPage": "string",
        "totalItems": 1,
        "totalPages": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> |  |
| `data[].channels` | array<string> |  |
| `data[].contact` | object |  |
| `data[].contact.email` | string |  |
| `data[].contact.fullName` | string |  |
| `data[].contact.id` | string |  |
| `data[].contactId` | string |  |
| `data[].createdAt` | string |  |
| `data[].createdBy` | string |  |
| `data[].haveReplies` | boolean |  |
| `data[].id` | string |  |
| `data[].isYourTurn` | boolean |  |
| `data[].lastActivityAt` | string |  |
| `data[].lastRepliedAt` | string |  |
| `data[].lastRepliedChannel` | string |  |
| `data[].lastRepliedSubject` | string |  |
| `data[].lastSentAt` | string |  |
| `data[].lastSentMessagePreview` | string |  |
| `data[].lastSentSubject` | string |  |
| `data[].opportunities` | array<string> |  |
| `data[].teamId` | string |  |
| `data[].users` | array<object> |  |
| `data[].users[].read` | boolean |  |
| `data[].users[].sender` | boolean |  |
| `data[].users[].userId` | string |  |
| `pagination` | object |  |
| `pagination.currentPage` | number |  |
| `pagination.nextPage` | string |  |
| `pagination.perPage` | number |  |
| `pagination.previousPage` | string |  |
| `pagination.totalItems` | number |  |
| `pagination.totalPages` | number |  |

## Native endpoint

Through the native lemlist API, this operation is `GET /inbox` (base URL `https://api.lemlist.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-inboxes.md) for the provider-specific parameters and requirements.

