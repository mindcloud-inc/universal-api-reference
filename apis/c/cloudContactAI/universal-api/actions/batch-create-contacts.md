# CloudContactAI: Batch Create Contacts



```
POST https://connect.mindcloud.co/v1/universal/cloudContactAI/latest/actions/batch-create-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CloudContactAI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/cloudContactAI/latest/actions/batch-create-contacts" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cloudContactAI/latest/actions/batch-create-contacts', {
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
      "clientId": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "firstName": "Ava",
      "id": "string",
      "lastName": "Chen",
      "phone": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `clientId` | number |  |
| `createdAt` | date |  |
| `email` | string |  |
| `firstName` | string |  |
| `id` | string |  |
| `lastName` | string |  |
| `phone` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native CloudContactAI API, this operation is `POST api/v2/contacts/batch` (base URL `https://core.cloudcontactai.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/batch-create-contacts.md) for the provider-specific parameters and requirements.

