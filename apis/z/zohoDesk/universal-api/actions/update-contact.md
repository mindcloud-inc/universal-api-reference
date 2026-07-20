# Zoho Desk: Update Contact



```
PUT https://connect.mindcloud.co/v1/universal/zohoDesk/latest/actions/update-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Desk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/zohoDesk/latest/actions/update-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contactId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoDesk/latest/actions/update-contact', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contactId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contactId` | string | yes | The Zoho Desk contact ID. |
| `firstName` | string | no | Updated first name for the contact. |

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

Through the native Zoho Desk API, this operation is `PATCH /contacts/[:contactId]` (base URL `https://desk.zoho.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-contact.md) for the provider-specific parameters and requirements.

