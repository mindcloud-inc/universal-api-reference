# SPS Commerce: List Packing Slips



```
GET https://connect.mindcloud.co/v1/universal/sPSCommerce/latest/actions/list-packing-slips
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SPS Commerce `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sPSCommerce/latest/actions/list-packing-slips?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sPSCommerce/latest/actions/list-packing-slips?${params}`, {
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
| `newest` | boolean | no |  |
| `name` | string | no |  |
| `limit` | string | no |  |
| `offset` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native SPS Commerce API returns.

## Native endpoint

Through the native SPS Commerce API, this operation is `GET packing-slip/v1/` (base URL `https://api.spscommerce.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-packing-slips.md) for the provider-specific parameters and requirements.

