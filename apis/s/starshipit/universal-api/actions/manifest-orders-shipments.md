# Starshipit: Manifest Orders (Shipments)



```
PUT https://connect.mindcloud.co/v1/universal/starshipit/latest/actions/manifest-orders-shipments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Starshipit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/starshipit/latest/actions/manifest-orders-shipments" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/starshipit/latest/actions/manifest-orders-shipments', {
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

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `trackingNumbers[]` | array<string> | no |  |
| `useOrderNumbers` | boolean | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "fileName": "Ava Chen",
      "pdf": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `fileName` | string |  |
| `pdf` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native Starshipit API, this operation is `POST /manifests/shipments` (base URL `https://api.starshipit.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/manifest-orders-shipments.md) for the provider-specific parameters and requirements.

