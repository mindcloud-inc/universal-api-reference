# i2i: List ship orders

Retrieves ship orders from i2i by status and date range.

```
GET https://connect.mindcloud.co/v1/universal/i2i/latest/actions/list-ship-orders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a i2i `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/i2i/latest/actions/list-ship-orders?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/i2i/latest/actions/list-ship-orders?${params}`, {
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
| `status` | string | no | Ship order status filter. One of: `0`, `1`, `2`, `3`, `4`, `5`, `6`, `7`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `startTime` | string | no | Earliest ship-order timestamp accepted by i2i for this lookup. Example: `2026-04-01T00:00:00Z`. |
| `endTime` | string | no | Latest ship-order timestamp accepted by i2i for this lookup. Example: `2026-04-28T23:59:59Z`. |
| `complete` | list | no | Completion flag filter used by i2i. One of: `0`, `1`. Default: `Y`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created": "string",
      "header": {
        "active": "string",
        "cancelled": "2026-05-07T12:00:00.000Z",
        "comment1": "string",
        "comment2": "string",
        "created": "2026-05-07T12:00:00.000Z",
        "id": 1,
        "number": "string",
        "opened": "2026-05-07T12:00:00.000Z",
        "packed": "2026-05-07T12:00:00.000Z",
        "picked": "2026-05-07T12:00:00.000Z",
        "poNo": "string",
        "refNo": "string",
        "service": "string",
        "shipped": "2026-05-07T12:00:00.000Z",
        "shipper": "string",
        "shipto": {
          "address1": "string",
          "address2": "string",
          "city": "Ava Chen",
          "code": "string",
          "contact": "Ava Chen",
          "country": "string",
          "email": "ava@example.com",
          "name": "Ava Chen",
          "postal": "string",
          "province": "string"
        },
        "soldto": {
          "address1": "string",
          "address2": "string",
          "city": "Ava Chen",
          "code": "string",
          "contact": "Ava Chen",
          "country": "string",
          "email": "ava@example.com",
          "name": "Ava Chen",
          "postal": "string",
          "province": "string"
        },
        "status": "string",
        "trackingNo": "string"
      },
      "id": 1,
      "lines": [
        {
          "description": "string",
          "item": "string",
          "orderedLot": "string",
          "orderedQty": 1,
          "pickedQty": 1,
          "picks": [
            {
              "pickedFrom": "string",
              "pickedLot": "string",
              "pickedQty": 1
            }
          ],
          "sentQty": 1
        }
      ],
      "number": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | string |  |
| `header.active` | string | Active flag returned by i2i. |
| `header.cancelled` | date | Cancellation timestamp when present. |
| `header.comment1` | string | First order comment. |
| `header.comment2` | string | Second order comment. |
| `header.created` | date | Created timestamp. |
| `header.id` | number | i2i ship order ID. |
| `header.number` | string | i2i ship order number. |
| `header.opened` | date | Opened timestamp. |
| `header.packed` | date | Packed timestamp. |
| `header.picked` | date | Picked timestamp. |
| `header.poNo` | string | Purchase order number. |
| `header.refNo` | string | Reference number. |
| `header.service` | string | Shipping service. |
| `header.shipped` | date | Shipped timestamp. |
| `header.shipper` | string | Shipper or carrier. |
| `header.shipto.address1` | string | Ship-to address line 1. |
| `header.shipto.address2` | string | Ship-to address line 2. |
| `header.shipto.city` | string | Ship-to city. |
| `header.shipto.code` | string | Ship-to code. |
| `header.shipto.contact` | string | Ship-to contact. |
| `header.shipto.country` | string | Ship-to country. |
| `header.shipto.email` | string | Ship-to email. |
| `header.shipto.name` | string | Ship-to name. |
| `header.shipto.postal` | string | Ship-to postal code. |
| `header.shipto.province` | string | Ship-to province. |
| `header.soldto.address1` | string | Sold-to address line 1. |
| `header.soldto.address2` | string | Sold-to address line 2. |
| `header.soldto.city` | string | Sold-to city. |
| `header.soldto.code` | string | Sold-to code. |
| `header.soldto.contact` | string | Sold-to contact. |
| `header.soldto.country` | string | Sold-to country. |
| `header.soldto.email` | string | Sold-to email. |
| `header.soldto.name` | string | Sold-to name. |
| `header.soldto.postal` | string | Sold-to postal code. |
| `header.soldto.province` | string | Sold-to province. |
| `header.status` | string | i2i ship order status. |
| `header.trackingNo` | string | Tracking number. |
| `id` | number |  |
| `lines[].description` | string | Line item description. |
| `lines[].item` | string | Line item code. |
| `lines[].orderedLot` | string | Ordered lot. |
| `lines[].orderedQty` | number | Ordered quantity. |
| `lines[].pickedQty` | number | Picked quantity. |
| `lines[].picks[].pickedFrom` | string | Picked-from location. |
| `lines[].picks[].pickedLot` | string | Picked lot. |
| `lines[].picks[].pickedQty` | number | Picked quantity for the pick record. |
| `lines[].sentQty` | number | Sent quantity. |
| `number` | string |  |
| `status` | string |  |

## Native endpoint

Through the native i2i API, this operation is `GET /ibis/api/v1.3/customers/{{credentials.consumerTag}}/ship/orders` (base URL `https://exch.i2i.ca`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-ship-orders.md) for the provider-specific parameters and requirements.

