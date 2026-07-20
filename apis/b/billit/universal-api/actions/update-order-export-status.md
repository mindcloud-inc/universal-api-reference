# Billit: Update Order Export Status

Updates a Billit order's export status and internal note.

```
PUT https://connect.mindcloud.co/v1/universal/billit/latest/actions/update-order-export-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Billit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/billit/latest/actions/update-order-export-status" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "orderID": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/billit/latest/actions/update-order-export-status', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "orderID": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `orderID` | number | yes | Billit OrderID to patch. |
| `IsSent` | boolean | no | Billit export flag described in the docs. |
| `InternalInfo` | string | no | Optional internal free-text note stored on the Billit order. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | string | Billit patch response payload. |

## Native endpoint

Through the native Billit API, this operation is `PATCH /v1/orders/:orderID` (base URL `https://api.sandbox.billit.be`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-order-export-status.md) for the provider-specific parameters and requirements.

