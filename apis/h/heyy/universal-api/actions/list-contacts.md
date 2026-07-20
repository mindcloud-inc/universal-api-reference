# Heyy: List Contacts

Retrieves contacts from a Heyy workspace.

```
GET https://connect.mindcloud.co/v1/universal/heyy/latest/actions/list-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Heyy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/heyy/latest/actions/list-contacts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/heyy/latest/actions/list-contacts?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": [
        {}
      ],
      "createdAt": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "firstName": "Ava",
      "fullName": "Ava Chen",
      "id": "string",
      "isSubscribed": true,
      "labels": [
        {}
      ],
      "lastName": "Chen",
      "phoneNumber": "string",
      "tenantId": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes` | array<object> |  |
| `createdAt` | date |  |
| `email` | string |  |
| `firstName` | string |  |
| `fullName` | string |  |
| `id` | string |  |
| `isSubscribed` | boolean |  |
| `labels` | array<object> |  |
| `lastName` | string |  |
| `phoneNumber` | string |  |
| `tenantId` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Heyy API, this operation is `GET /contacts` (base URL `https://api.heyy.io/api/v2.0/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-contacts.md) for the provider-specific parameters and requirements.

