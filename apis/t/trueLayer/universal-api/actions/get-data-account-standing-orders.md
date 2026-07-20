# TrueLayer: Get Data Account Standing Orders

Retrieves data account standing orders from TrueLayer.

```
GET https://connect.mindcloud.co/v1/universal/trueLayer/latest/actions/get-data-account-standing-orders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TrueLayer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/trueLayer/latest/actions/get-data-account-standing-orders?connectionId=$CONNECTION_ID&account_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "account_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/trueLayer/latest/actions/get-data-account-standing-orders?${params}`, {
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
| `account_id` | string | yes | TrueLayer Data API account ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": 1,
      "currency": "string",
      "name": "Ava Chen",
      "standing_order_id": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | number |  |
| `currency` | string |  |
| `name` | string |  |
| `standing_order_id` | string |  |
| `status` | string |  |

## Native endpoint

Through the native TrueLayer API, this operation is `GET /data/v1/accounts/:account_id/standing_orders` (base URL `https://api.truelayer-sandbox.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-data-account-standing-orders.md) for the provider-specific parameters and requirements.

