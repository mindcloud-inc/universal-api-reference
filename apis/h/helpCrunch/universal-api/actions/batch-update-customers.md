# HelpCrunch: Batch Update Customers

Updates multiple customer records in HelpCrunch.

```
PUT https://connect.mindcloud.co/v1/universal/helpCrunch/latest/actions/batch-update-customers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HelpCrunch `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/helpCrunch/latest/actions/batch-update-customers" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/helpCrunch/latest/actions/batch-update-customers', {
  method: 'PUT',
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
      "blocked": true,
      "company": "string",
      "createdFrom": "string",
      "customData": {},
      "device": {},
      "email": "ava@example.com",
      "firstSeen": "string",
      "id": 1,
      "integrationId": "string",
      "lastPage": "string",
      "lastSeen": "string",
      "locale": "string",
      "location": {},
      "name": "Ava Chen",
      "notes": "string",
      "phone": "string",
      "referer": "string",
      "source": "string",
      "tags": [
        {}
      ],
      "unsubscribed": true,
      "userId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `blocked` | boolean |  |
| `company` | string |  |
| `createdFrom` | string |  |
| `customData` | object |  |
| `device` | object |  |
| `email` | string |  |
| `firstSeen` | string |  |
| `id` | number |  |
| `integrationId` | string |  |
| `lastPage` | string |  |
| `lastSeen` | string |  |
| `locale` | string |  |
| `location` | object |  |
| `name` | string |  |
| `notes` | string |  |
| `phone` | string |  |
| `referer` | string |  |
| `source` | string |  |
| `tags` | array<object> |  |
| `unsubscribed` | boolean |  |
| `userId` | string |  |

## Native endpoint

Through the native HelpCrunch API, this operation is `PUT /customers/batch` (base URL `https://api.helpcrunch.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/batch-update-customers.md) for the provider-specific parameters and requirements.

