# Faire: Add Shipments to Order



```
POST https://connect.mindcloud.co/v1/universal/Faire/latest/actions/add-shipments-to-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Faire `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/Faire/latest/actions/add-shipments-to-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "orderId": "bo_bxdmjbwxid"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/Faire/latest/actions/add-shipments-to-order', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "orderId": "bo_bxdmjbwxid"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `orderId` | string | yes | The ID of the order to add shipments to. Example: `bo_bxdmjbwxid`. |
| `shipments[]` | array<object> | no | A list of shipments to add to the order. Accepts multiple values as an array. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `shipments[].orderId` | string | no | The ID of the order the shipment is attached to. Example: `bo_bxdmjbwxid`. |
| `shipments[].carrier` | string | no | The carrier used to ship the order. Accepted values are case insensitive; Faire may also attempt to recognize other carrier names. Carriers: CANADA_POST, DHL_ECOMMERCE, DHL_EXPRESS, FEDEX, PUROLATOR, UPS, USPS, POSTNL, CANPAR, INTERLINK_EXPRESS, GSO, ROYAL_MAIL, DPD, DPDUK, PARCELFORCE, AUSTRALIA_POST, EVRI, and LA_POSTE Example: `fedex`. |
| `shipments[].trackingCode` | string | no | The tracking code for the shipment; its format varies by carrier. Example: `94029300101029282`. |
| `shipments[].makerCost` | object | no | The cost the brand paid to ship the order. |
| `shipments[].makerCost.amountMinor` | number | no | The amount in the smallest unit of the currency, such as cents for USD. Example: `4999`. |
| `shipments[].makerCost.currency` | string | no | The currency in ISO 4217 format, such as USD. Example: `USD`. |
| `shipments[].shippingType` | list<string> | no | How the shipment is handled: the brand ships it or uses Faire's shipping service. One of: `SHIP_ON_YOUR_OWN`, `SHIP_WITH_FAIRE`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Faire API returns.

## Native endpoint

Through the native Faire API, this operation is `POST orders/:orderId/shipments` (base URL `https://www.faire.com/external-api/v2/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-shipments-to-order.md) for the provider-specific parameters and requirements.

