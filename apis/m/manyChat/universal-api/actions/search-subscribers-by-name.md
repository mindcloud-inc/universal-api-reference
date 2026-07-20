# ManyChat: Search Subscribers by Name

Finds subscribers in ManyChat by name.

```
GET https://connect.mindcloud.co/v1/universal/manyChat/latest/actions/search-subscribers-by-name
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ManyChat `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/manyChat/latest/actions/search-subscribers-by-name?connectionId=$CONNECTION_ID&name=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "name": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/manyChat/latest/actions/search-subscribers-by-name?${params}`, {
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
| `name` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {
          "customFields": [
            {
              "description": "string",
              "id": 1,
              "name": "Ava Chen",
              "type": "string",
              "value": "string"
            }
          ],
          "email": "ava@example.com",
          "firstName": "Ava",
          "gender": "string",
          "id": "string",
          "igId": 1,
          "igUsername": "Ava Chen",
          "isFollowupEnabled": true,
          "language": "string",
          "lastInputText": "string",
          "lastInteraction": "2026-05-07T12:00:00.000Z",
          "lastName": "Chen",
          "lastSeen": "2026-05-07T12:00:00.000Z",
          "liveChatUrl": "https://example.com",
          "locale": "string",
          "name": "Ava Chen",
          "optinEmail": true,
          "optinPhone": true,
          "optinWhatsapp": true,
          "pageId": "string",
          "phone": "string",
          "profilePic": "string",
          "subscribed": "2026-05-07T12:00:00.000Z",
          "tags": [
            {
              "id": 1,
              "name": "Ava Chen"
            }
          ],
          "timezone": "string",
          "userRefs": [
            {
              "optedIn": "2026-05-07T12:00:00.000Z",
              "userRef": "string"
            }
          ],
          "whatsappPhone": "string"
        }
      ],
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> |  |
| `data[].customFields` | array<object> |  |
| `data[].customFields[].description` | string |  |
| `data[].customFields[].id` | number |  |
| `data[].customFields[].name` | string |  |
| `data[].customFields[].type` | string |  |
| `data[].customFields[].value` | string |  |
| `data[].email` | string |  |
| `data[].firstName` | string |  |
| `data[].gender` | string |  |
| `data[].id` | string |  |
| `data[].igId` | number |  |
| `data[].igUsername` | string |  |
| `data[].isFollowupEnabled` | boolean |  |
| `data[].language` | string |  |
| `data[].lastInputText` | string |  |
| `data[].lastInteraction` | date |  |
| `data[].lastName` | string |  |
| `data[].lastSeen` | date |  |
| `data[].liveChatUrl` | string |  |
| `data[].locale` | string |  |
| `data[].name` | string |  |
| `data[].optinEmail` | boolean |  |
| `data[].optinPhone` | boolean |  |
| `data[].optinWhatsapp` | boolean |  |
| `data[].pageId` | string |  |
| `data[].phone` | string |  |
| `data[].profilePic` | string |  |
| `data[].subscribed` | date |  |
| `data[].tags` | array<object> |  |
| `data[].tags[].id` | number |  |
| `data[].tags[].name` | string |  |
| `data[].timezone` | string |  |
| `data[].userRefs` | array<object> |  |
| `data[].userRefs[].optedIn` | date |  |
| `data[].userRefs[].userRef` | string |  |
| `data[].whatsappPhone` | string |  |
| `status` | string |  |

## Native endpoint

Through the native ManyChat API, this operation is `GET /fb/subscriber/findByName` (base URL `https://api.manychat.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-subscribers-by-name.md) for the provider-specific parameters and requirements.

