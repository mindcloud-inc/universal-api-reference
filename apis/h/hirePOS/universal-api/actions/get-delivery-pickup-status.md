# HirePOS: Get Delivery Pickup Status

Retrieves delivery and pickup status for an invoice from HirePOS.

```
GET https://connect.mindcloud.co/v1/universal/hirePOS/latest/actions/get-delivery-pickup-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HirePOS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hirePOS/latest/actions/get-delivery-pickup-status?connectionId=$CONNECTION_ID&invoiceNo=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "invoiceNo": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hirePOS/latest/actions/get-delivery-pickup-status?${params}`, {
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
| `invoiceNo` | string | yes | Invoice number to retrieve delivery and pickup status for. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native HirePOS API returns.

## Native endpoint

Through the native HirePOS API, this operation is `GET /DeliveryPickupStatus` (base URL `https://api.hirepos.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-delivery-pickup-status.md) for the provider-specific parameters and requirements.

