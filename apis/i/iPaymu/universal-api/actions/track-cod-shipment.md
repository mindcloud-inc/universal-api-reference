# iPaymu: Track COD Shipment

Track the status of an iPaymu cash-on-delivery shipment.

```
GET https://connect.mindcloud.co/v1/universal/iPaymu/latest/actions/track-cod-shipment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a iPaymu `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/iPaymu/latest/actions/track-cod-shipment?connectionId=$CONNECTION_ID&awb=string&transaction_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "awb": "string",
  "transaction_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/iPaymu/latest/actions/track-cod-shipment?${params}`, {
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
| `awb` | string | yes | Air waybill / tracking number. |
| `transaction_id` | string | yes | COD transaction identifier. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native iPaymu API returns.

## Native endpoint

Through the native iPaymu API, this operation is `POST /cod/tracking` (base URL `https://my.ipaymu.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/track-cod-shipment.md) for the provider-specific parameters and requirements.

