# Restoplace: Get Hall

Retrieves a hall from Restoplace.

```
GET https://connect.mindcloud.co/v1/universal/restoplace/latest/actions/get-hall
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Restoplace `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/restoplace/latest/actions/get-hall?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/restoplace/latest/actions/get-hall?${params}`, {
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
| `id` | number | yes | Unique Restoplace hall ID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Restoplace API returns.

## Native endpoint

Through the native Restoplace API, this operation is `GET /halls/:id` (base URL `https://api.restoplace.cc`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-hall.md) for the provider-specific parameters and requirements.

