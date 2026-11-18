# Wayfair: Get Bill of Lading



```
GET https://connect.mindcloud.co/v1/universal/wayfair/latest/actions/get-bill-of-lading
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wayfair `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wayfair/latest/actions/get-bill-of-lading?connectionId=$CONNECTION_ID&purchaseOrderNumber=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "purchaseOrderNumber": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wayfair/latest/actions/get-bill-of-lading?${params}`, {
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
| `purchaseOrderNumber` | string | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Wayfair API returns.

## Native endpoint

Through the native Wayfair API, this operation is `GET bill_of_lading/:purchaseOrderNumber` (base URL `https://{{credentials.environment}}.com/v1/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-bill-of-lading.md) for the provider-specific parameters and requirements.

