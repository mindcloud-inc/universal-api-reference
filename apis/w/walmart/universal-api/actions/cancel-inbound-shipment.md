# Walmart: Cancel Inbound Shipment

Cancel an inbound shipment order.

```
DELETE https://connect.mindcloud.co/v1/universal/walmart/latest/actions/cancel-inbound-shipment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Walmart `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/walmart/latest/actions/cancel-inbound-shipment?connectionId=$CONNECTION_ID&inboundOrderId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "inboundOrderId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/walmart/latest/actions/cancel-inbound-shipment?${params}`, {
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
| `inboundOrderId` | string | yes | Unique ID identifying inbound shipment request. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `status` | string | Returns "OK" on success |

## Native endpoint

Through the native Walmart API, this operation is `DELETE /v3/fulfillment/inbound-shipments/:inboundOrderId` (base URL `https://{{credentials.environment}}.walmartapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/cancel-inbound-shipment.md) for the provider-specific parameters and requirements.

