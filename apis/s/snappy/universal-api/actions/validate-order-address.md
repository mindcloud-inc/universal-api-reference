# Snappy: Validate Order Address

Validates a shipping address in Snappy.

```
GET https://connect.mindcloud.co/v1/universal/snappy/latest/actions/validate-order-address
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Snappy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/snappy/latest/actions/validate-order-address?connectionId=$CONNECTION_ID&address=%5Bobject%20Object%5D&companyId=string&country=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "address": "[object Object]",
  "companyId": "string",
  "country": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/snappy/latest/actions/validate-order-address?${params}`, {
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
| `address` | object | yes |  |
| `companyId` | string | yes |  |
| `country` | string | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Snappy API returns.

## Native endpoint

Through the native Snappy API, this operation is `POST /orders/addresses/validate` (base URL `https://api.snappy.com/public-api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/validate-order-address.md) for the provider-specific parameters and requirements.

