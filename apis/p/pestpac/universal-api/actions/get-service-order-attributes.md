# PestPac: Get Service Order Attributes



```
GET https://connect.mindcloud.co/v1/universal/pestpac/latest/actions/get-service-order-attributes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PestPac `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pestpac/latest/actions/get-service-order-attributes?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pestpac/latest/actions/get-service-order-attributes?${params}`, {
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
| `orderId` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native PestPac API returns.

## Native endpoint

Through the native PestPac API, this operation is `GET ServiceOrders/:orderId/attributes` (base URL `https://api.workwave.com/pestpac/v1/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-service-order-attributes.md) for the provider-specific parameters and requirements.

