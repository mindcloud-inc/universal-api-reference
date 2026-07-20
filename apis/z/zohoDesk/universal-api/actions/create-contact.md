# Zoho Desk: Create Contact



```
POST https://connect.mindcloud.co/v1/universal/zohoDesk/latest/actions/create-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Desk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zohoDesk/latest/actions/create-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "lastName": "Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoDesk/latest/actions/create-contact', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "lastName": "Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `lastName` | string | yes | Last name for the new contact. |
| `email` | string | no | Email for the new contact. |

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

Through the native Zoho Desk API, this operation is `POST /contacts` (base URL `https://desk.zoho.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-contact.md) for the provider-specific parameters and requirements.

