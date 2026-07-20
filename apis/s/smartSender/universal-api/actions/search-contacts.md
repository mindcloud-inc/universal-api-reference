# Smart Sender: Search Contacts

Finds contacts in Smart Sender by keyword.

```
GET https://connect.mindcloud.co/v1/universal/smartSender/latest/actions/search-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Smart Sender `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smartSender/latest/actions/search-contacts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smartSender/latest/actions/search-contacts?${params}`, {
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
| `term` | string | no | Keyword used to search contacts. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "channels": [
        {}
      ],
      "email": "ava@example.com",
      "firstName": "Ava",
      "fullName": "Ava Chen",
      "id": 1,
      "identifier": "string",
      "lastName": "Chen",
      "notes": "string",
      "phone": "string",
      "tags": [
        {}
      ],
      "variables": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `channels` | array<object> |  |
| `email` | string |  |
| `firstName` | string |  |
| `fullName` | string |  |
| `id` | number |  |
| `identifier` | string |  |
| `lastName` | string |  |
| `notes` | string |  |
| `phone` | string |  |
| `tags` | array<object> |  |
| `variables` | array<object> |  |

## Native endpoint

Through the native Smart Sender API, this operation is `GET /v1/contacts/search` (base URL `https://api.smartsender.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-contacts.md) for the provider-specific parameters and requirements.

