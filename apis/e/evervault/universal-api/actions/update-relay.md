# Evervault: Update Relay

Updates an existing relay in Evervault.

```
PUT https://connect.mindcloud.co/v1/universal/evervault/latest/actions/update-relay
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Evervault `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/evervault/latest/actions/update-relay" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/evervault/latest/actions/update-relay', {
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
      "app": "string",
      "authentication": "string",
      "createdAt": 1,
      "destinationDomain": "string",
      "encryptEmptyStrings": true,
      "evervaultDomain": "string",
      "id": "string",
      "routes": [
        {}
      ],
      "updatedAt": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `app` | string |  |
| `authentication` | string |  |
| `createdAt` | number |  |
| `destinationDomain` | string |  |
| `encryptEmptyStrings` | boolean |  |
| `evervaultDomain` | string |  |
| `id` | string |  |
| `routes` | array<object> |  |
| `updatedAt` | number |  |

## Native endpoint

Through the native Evervault API, this operation is `PATCH /relays/{id}` (base URL `https://api.evervault.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-relay.md) for the provider-specific parameters and requirements.

