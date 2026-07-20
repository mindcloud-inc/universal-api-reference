# Vouchery.io: Get Rule



```
GET https://connect.mindcloud.co/v1/universal/voucheryio/latest/actions/get-rule
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vouchery.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/voucheryio/latest/actions/get-rule?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/voucheryio/latest/actions/get-rule?${params}`, {
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
| `id` | number | yes | Rule ID from the path. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Vouchery.io API returns.

## Native endpoint

Through the native Vouchery.io API, this operation is `GET /rules/:id` (base URL `https://mindcloud.sandbox.vouchery.app/api/v2.1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-rule.md) for the provider-specific parameters and requirements.

