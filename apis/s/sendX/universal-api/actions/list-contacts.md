# SendX: List Contacts



```
GET https://connect.mindcloud.co/v1/universal/sendX/latest/actions/list-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SendX `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sendX/latest/actions/list-contacts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sendX/latest/actions/list-contacts?${params}`, {
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
| `search` | string | no | Search contacts by first name, last name, or email. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "blocked": true,
      "bounced": true,
      "company": "string",
      "contactSource": 1,
      "created": "2026-05-07T12:00:00.000Z",
      "customFields": {},
      "dropped": true,
      "email": "ava@example.com",
      "firstName": "Ava",
      "id": "string",
      "lastName": "Chen",
      "lastTrackedIp": "string",
      "lists": [
        "string"
      ],
      "LTV": 1,
      "pageSource": "string",
      "spam": true,
      "tags": [
        "string"
      ],
      "trackData": "string",
      "unsubscribed": true,
      "updated": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `blocked` | boolean |  |
| `bounced` | boolean |  |
| `company` | string |  |
| `contactSource` | number |  |
| `created` | date |  |
| `customFields` | object |  |
| `dropped` | boolean |  |
| `email` | string |  |
| `firstName` | string |  |
| `id` | string |  |
| `lastName` | string |  |
| `lastTrackedIp` | string |  |
| `lists` | array<string> |  |
| `LTV` | number |  |
| `pageSource` | string |  |
| `spam` | boolean |  |
| `tags` | array<string> |  |
| `trackData` | string |  |
| `unsubscribed` | boolean |  |
| `updated` | date |  |

## Native endpoint

Through the native SendX API, this operation is `GET /contact` (base URL `https://api.sendx.io/api/v1/rest`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-contacts.md) for the provider-specific parameters and requirements.

