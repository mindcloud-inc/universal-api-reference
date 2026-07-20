# Eventee: Create Partner

Creates a partner in Eventee.

```
POST https://connect.mindcloud.co/v1/universal/eventee/latest/actions/create-partner
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Eventee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/eventee/latest/actions/create-partner" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/eventee/latest/actions/create-partner', {
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
      "company": "string",
      "description": "string",
      "email": "ava@example.com",
      "exhibitor_info": {},
      "id": 1,
      "phone": "string",
      "sponsor_info": {},
      "web": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | string |  |
| `company` | string |  |
| `description` | string |  |
| `email` | string |  |
| `exhibitor_info` | object |  |
| `id` | number |  |
| `phone` | string |  |
| `sponsor_info` | object |  |
| `web` | string |  |

## Native endpoint

Through the native Eventee API, this operation is `POST /partner` (base URL `https://api.eventee.com/public/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-partner.md) for the provider-specific parameters and requirements.

