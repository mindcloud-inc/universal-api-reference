# Dachser: Create Transport Order

Creates a new transport order in Dachser.

```
POST https://connect.mindcloud.co/v1/universal/dachser/latest/actions/create-transport-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dachser `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/dachser/latest/actions/create-transport-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "basket": "string",
  "transportDate": "2026-05-07T12:00:00.000Z",
  "division": "string",
  "product": "string",
  "term": "string",
  "consignee": {},
  "transportOrderLines[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dachser/latest/actions/create-transport-order', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "basket": "string",
    "transportDate": "2026-05-07T12:00:00.000Z",
    "division": "string",
    "product": "string",
    "term": "string",
    "consignee": {},
    "transportOrderLines[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `basket` | string | yes | Transport order basket. |
| `transportDate` | date | yes | Date when the goods shall be picked up. |
| `division` | string | yes | DACHSER division. Use T for industrial goods or F for food. |
| `product` | string | yes | DACHSER product code. |
| `term` | string | yes | Terms of delivery for European Logistics. |
| `consignee` | object | yes | Receiver of the consignment. |
| `transportOrderLines[]` | array<object> | yes | Detailed goods lines to be transported. |
| `labelFormat` | string | no | Label format. Use P for PDF or Z for ZPL. Default: `P`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `forwarder` | object | no | DACHSER branch that collects and dispatches the consignment. |
| `consignor` | object | no | Sender or pickup customer. |
| `transportOptions` | object | no | Optional DACHSER transport options. |
| `goodsValueInsurance` | object | no | Goods value insurance amount. |
| `references[]` | array<object> | no | Customer order, delivery note, and other references. |
| `furtherAddresses[]` | array<object> | no | Optional loading points, cover addresses, and other addresses. |
| `packingAids[]` | array<object> | no | Optional packing aids. |
| `texts[]` | array<object> | no | Additional texts for driver, invoice, or delivery note. |
| `orderGroup` | string | no | Order group for invoice splitting. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "label": "string",
      "links": [
        {}
      ],
      "messages": [
        "string"
      ],
      "ssccs": [
        "string"
      ],
      "state": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |
| `label` | string |  |
| `links` | array<object> |  |
| `messages` | array<string> |  |
| `ssccs` | array<string> |  |
| `state` | string |  |

## Native endpoint

Through the native Dachser API, this operation is `POST /rest/v2/transportorders/{basket}` (base URL `https://api-gateway.dachser.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-transport-order.md) for the provider-specific parameters and requirements.

