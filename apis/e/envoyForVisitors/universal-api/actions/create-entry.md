# Envoy for Visitors: Create Entry

Creates a new entry in Envoy for Visitors.

```
POST https://connect.mindcloud.co/v1/universal/envoyForVisitors/latest/actions/create-entry
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Envoy for Visitors `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/envoyForVisitors/latest/actions/create-entry" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/envoyForVisitors/latest/actions/create-entry', {
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
      "agreementsStatus": "string",
      "customFields": [
        {}
      ],
      "email": "ava@example.com",
      "flowId": "string",
      "fullName": "Ava Chen",
      "id": "string",
      "isDelivery": true,
      "locationId": "string",
      "signedInAt": "2026-05-07T12:00:00.000Z",
      "signedInVia": "string",
      "signedOutAt": "2026-05-07T12:00:00.000Z",
      "signedOutVia": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `agreementsStatus` | string |  |
| `customFields` | array<object> |  |
| `email` | string |  |
| `flowId` | string |  |
| `fullName` | string |  |
| `id` | string |  |
| `isDelivery` | boolean |  |
| `locationId` | string |  |
| `signedInAt` | date |  |
| `signedInVia` | string |  |
| `signedOutAt` | date |  |
| `signedOutVia` | string |  |

## Native endpoint

Through the native Envoy for Visitors API, this operation is `POST /entries` (base URL `https://api.envoy.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-entry.md) for the provider-specific parameters and requirements.

