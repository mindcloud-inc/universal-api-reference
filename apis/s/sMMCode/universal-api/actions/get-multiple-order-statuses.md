# SMMCode: Get Multiple Order Statuses



```
GET https://connect.mindcloud.co/v1/universal/sMMCode/latest/actions/get-multiple-order-statuses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SMMCode `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sMMCode/latest/actions/get-multiple-order-statuses?connectionId=$CONNECTION_ID&orders=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "orders": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sMMCode/latest/actions/get-multiple-order-statuses?${params}`, {
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
| `orders` | string | yes | Order IDs separated by commas. Accepts multiple values in one string, delimited by `,`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native SMMCode API returns.

## Native endpoint

Through the native SMMCode API, this operation is `POST /api/v2` (base URL `https://extended.smmcode.org`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-multiple-order-statuses.md) for the provider-specific parameters and requirements.

