# 2Chat: List Contacts

Retrieves contact records from 2Chat.

```
GET https://connect.mindcloud.co/v1/universal/chat/latest/actions/list-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 2Chat `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chat/latest/actions/list-contacts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chat/latest/actions/list-contacts?${params}`, {
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
| `channelUuid` | string | no | Limit results to a specific WhatsApp channel UUID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contacts": [
        {
          "channelUuid": {},
          "details": [
            {
              "createdAt": "2026-05-07T12:00:00.000Z",
              "createdAtTimestamp": "2026-05-07T12:00:00.000Z",
              "type": "string",
              "value": "string"
            }
          ],
          "firstName": "Ava",
          "lastName": "Chen",
          "lastUpdated": "2026-05-07T12:00:00.000Z",
          "name": "Ava Chen",
          "profilePicUrl": {},
          "uuid": "string"
        }
      ],
      "count": 1,
      "page": 1,
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contacts[].channelUuid` | object |  |
| `contacts[].details[].createdAt` | date |  |
| `contacts[].details[].createdAtTimestamp` | date |  |
| `contacts[].details[].type` | string |  |
| `contacts[].details[].value` | string |  |
| `contacts[].firstName` | string |  |
| `contacts[].lastName` | string |  |
| `contacts[].lastUpdated` | date |  |
| `contacts[].name` | string |  |
| `contacts[].profilePicUrl` | object |  |
| `contacts[].uuid` | string |  |
| `count` | number |  |
| `page` | number |  |
| `success` | boolean |  |

## Native endpoint

Through the native 2Chat API, this operation is `GET /contacts` (base URL `https://api.p.2chat.io/open`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-contacts.md) for the provider-specific parameters and requirements.

