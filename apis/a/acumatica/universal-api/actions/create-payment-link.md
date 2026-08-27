# Acumatica: Create Payment Link

Creates a Payment Link for an Sales Order

```
POST https://connect.mindcloud.co/v1/universal/acumatica/latest/actions/create-payment-link
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Acumatica `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/acumatica/latest/actions/create-payment-link" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "wse": "string",
  "endpointVersion": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/acumatica/latest/actions/create-payment-link', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "wse": "string",
    "endpointVersion": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `entity` | object | no |  |
| `entity.OrderNbr.value` | string | no |  |
| `entity.OrderType` | object | no |  |
| `entity.OrderType.value` | string | no |  |
| `entity.OrderNbr` | object | no |  |
| `wse` | string | yes |  |
| `endpointVersion` | string | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Acumatica API returns.

## Native endpoint

Through the native Acumatica API, this operation is `POST /entity/:wse/:endpointVersion/SalesOrder/CreateLink` (base URL `{{credentials.uRL}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-payment-link.md) for the provider-specific parameters and requirements.

