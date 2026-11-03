# Rithum for Brands: Mark Order Exported

Mark an Order as Exported.

```
GET https://connect.mindcloud.co/v1/universal/rithumForBrands/latest/actions/post-order-exported
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rithum for Brands `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rithumForBrands/latest/actions/post-order-exported?connectionId=$CONNECTION_ID&orderID=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "orderID": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rithumForBrands/latest/actions/post-order-exported?${params}`, {
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
| `orderID` | string | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Rithum for Brands API returns.

## Native endpoint

Through the native Rithum for Brands API, this operation is `POST Orders(:orderID)/Export` (base URL `https://api.channeladvisor.com/v1/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/post-order-exported.md) for the provider-specific parameters and requirements.

