# Amark: Get Order Info



```
GET https://connect.mindcloud.co/v1/universal/amarkAWL/latest/actions/get-order-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Amark `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/amarkAWL/latest/actions/get-order-info?connectionId=$CONNECTION_ID&orderNumber=string&orderId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "orderNumber": "string",
  "orderId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/amarkAWL/latest/actions/get-order-info?${params}`, {
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
| `orderNumber` | string | yes | Required. Enter the Order Number that matches the Order ID. |
| `orderId` | number | yes | Required. Enter the numeric Order ID that matches the Order Number. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Amark API returns.

## Native endpoint

Through the native Amark API, this operation is `POST /Order/Info` (base URL `{{credentials.environment}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-order-info.md) for the provider-specific parameters and requirements.

