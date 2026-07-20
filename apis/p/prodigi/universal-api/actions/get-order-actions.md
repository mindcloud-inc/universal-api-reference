# Prodigi: Get Order Actions

Retrieves available actions for a Prodigi order.

```
GET https://connect.mindcloud.co/v1/universal/prodigi/latest/actions/get-order-actions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Prodigi `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/prodigi/latest/actions/get-order-actions?connectionId=$CONNECTION_ID&prodigiOrderId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "prodigiOrderId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/prodigi/latest/actions/get-order-actions?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `prodigiOrderId` | string | yes | Prodigi order ID, such as ord_123456. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cancel": {},
      "changeMetaData": {},
      "changeRecipientDetails": {},
      "changeShippingMethod": {},
      "outcome": "string",
      "traceParent": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cancel` | object | Cancel action availability and details. |
| `changeMetaData` | object | Metadata update action availability and details. |
| `changeRecipientDetails` | object | Recipient update action availability and details. |
| `changeShippingMethod` | object | Shipping-method update action availability and details. |
| `outcome` | string | Actions lookup outcome. |
| `traceParent` | string | Prodigi trace identifier. |

## Native endpoint

Through the native Prodigi API, this operation is `GET /orders/[:prodigiOrderId]/actions` (base URL `https://api.prodigi.com/v4.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-order-actions.md) for the provider-specific parameters and requirements.

