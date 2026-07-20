# Merit: List Payment Types



```
GET https://connect.mindcloud.co/v1/universal/merit/latest/actions/list-payment-types
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Merit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/merit/latest/actions/list-payment-types?connectionId=$CONNECTION_ID&type=3" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "type": "3"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/merit/latest/actions/list-payment-types?${params}`, {
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
| `type` | number | yes | Example: `3`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Merit API returns.

## Native endpoint

Through the native Merit API, this operation is `POST v2/getpaymenttypes` (base URL `https://aktiva.merit.ee/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-payment-types.md) for the provider-specific parameters and requirements.

