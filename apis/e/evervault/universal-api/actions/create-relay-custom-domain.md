# Evervault: Create Relay Custom Domain

Creates a relay custom domain in Evervault.

```
POST https://connect.mindcloud.co/v1/universal/evervault/latest/actions/create-relay-custom-domain
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Evervault `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/evervault/latest/actions/create-relay-custom-domain" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/evervault/latest/actions/create-relay-custom-domain', {
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
      "createdAt": 1,
      "customDomain": "string",
      "id": "string",
      "relay": "string",
      "status": "string",
      "updatedAt": 1,
      "validationRecord": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | number |  |
| `customDomain` | string |  |
| `id` | string |  |
| `relay` | string |  |
| `status` | string |  |
| `updatedAt` | number |  |
| `validationRecord` | object |  |

## Native endpoint

Through the native Evervault API, this operation is `POST /relays/{relay_id}/custom-domains` (base URL `https://api.evervault.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-relay-custom-domain.md) for the provider-specific parameters and requirements.

