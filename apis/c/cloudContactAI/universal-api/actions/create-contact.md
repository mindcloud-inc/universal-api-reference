# CloudContactAI: Create Contact



```
POST https://connect.mindcloud.co/v1/universal/cloudContactAI/latest/actions/create-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CloudContactAI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/cloudContactAI/latest/actions/create-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cloudContactAI/latest/actions/create-contact', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "blockIncomingSMS": true,
      "clientExternalId": "string",
      "clientId": 1,
      "collectionInfo": {},
      "createdAt": "2026-05-07T12:00:00.000Z",
      "data": {},
      "disabledAt": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "enableBotResponse": true,
      "firstName": "Ava",
      "id": "string",
      "lastName": "Chen",
      "lists": [
        {}
      ],
      "notes": "string",
      "originalPhone": "string",
      "pending": 1,
      "phone": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "userClientId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `blockIncomingSMS` | boolean |  |
| `clientExternalId` | string |  |
| `clientId` | number |  |
| `collectionInfo` | object |  |
| `createdAt` | date |  |
| `data` | object |  |
| `disabledAt` | date |  |
| `email` | string |  |
| `enableBotResponse` | boolean |  |
| `firstName` | string |  |
| `id` | string |  |
| `lastName` | string |  |
| `lists` | array<object> |  |
| `notes` | string |  |
| `originalPhone` | string |  |
| `pending` | number |  |
| `phone` | string |  |
| `updatedAt` | date |  |
| `userClientId` | string |  |

## Native endpoint

Through the native CloudContactAI API, this operation is `POST api/v2/contacts` (base URL `https://core.cloudcontactai.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-contact.md) for the provider-specific parameters and requirements.

