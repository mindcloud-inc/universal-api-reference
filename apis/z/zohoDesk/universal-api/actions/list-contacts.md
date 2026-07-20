# Zoho Desk: List Contacts



```
GET https://connect.mindcloud.co/v1/universal/zohoDesk/latest/actions/list-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Desk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoDesk/latest/actions/list-contacts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoDesk/latest/actions/list-contacts?${params}`, {
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
      "accountId": "string",
      "createdTime": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "firstName": "Ava",
      "id": "string",
      "isEndUser": true,
      "isSpam": true,
      "lastName": "Chen",
      "mobile": "string",
      "modifiedTime": "2026-05-07T12:00:00.000Z",
      "phone": "string",
      "webUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | string |  |
| `createdTime` | date |  |
| `email` | string |  |
| `firstName` | string |  |
| `id` | string |  |
| `isEndUser` | boolean |  |
| `isSpam` | boolean |  |
| `lastName` | string |  |
| `mobile` | string |  |
| `modifiedTime` | date |  |
| `phone` | string |  |
| `webUrl` | string |  |

## Native endpoint

Through the native Zoho Desk API, this operation is `GET /contacts` (base URL `https://desk.zoho.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-contacts.md) for the provider-specific parameters and requirements.

