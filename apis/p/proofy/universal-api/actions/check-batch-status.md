# Proofy: Check Batch Status



```
GET https://connect.mindcloud.co/v1/universal/proofy/latest/actions/check-batch-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Proofy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/proofy/latest/actions/check-batch-status?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/proofy/latest/actions/check-batch-status?${params}`, {
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
| `id` | string | yes | Batch request identifier. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Proofy API returns.

## Native endpoint

Through the native Proofy API, this operation is `GET /verify/batch/:id` (base URL `https://apis.proofy.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/check-batch-status.md) for the provider-specific parameters and requirements.

