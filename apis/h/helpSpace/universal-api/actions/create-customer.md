# HelpSpace: Create Customer

Creates a new customer in HelpSpace.

```
POST https://connect.mindcloud.co/v1/universal/helpSpace/latest/actions/create-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HelpSpace `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/helpSpace/latest/actions/create-customer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/helpSpace/latest/actions/create-customer', {
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
      "address": "string",
      "city": "string",
      "country": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "customFields": {},
      "email": "ava@example.com",
      "id": 1,
      "jobTitle": "string",
      "locale": "string",
      "name": "Ava Chen",
      "note": "string",
      "postalCode": "string",
      "state": "string",
      "timezone": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | string |  |
| `city` | string |  |
| `country` | string |  |
| `createdAt` | date |  |
| `customFields` | object |  |
| `email` | string |  |
| `id` | number |  |
| `jobTitle` | string |  |
| `locale` | string |  |
| `name` | string |  |
| `note` | string |  |
| `postalCode` | string |  |
| `state` | string |  |
| `timezone` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native HelpSpace API, this operation is `POST /customers` (base URL `https://api.helpspace.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-customer.md) for the provider-specific parameters and requirements.

