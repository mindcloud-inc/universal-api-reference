# fal.ai: Flush Application Queue

Deletes pending requests from a fal.ai application queue.

```
DELETE https://connect.mindcloud.co/v1/universal/falai/latest/actions/flush-application-queue
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a fal.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/falai/latest/actions/flush-application-queue?connectionId=$CONNECTION_ID&name=Ava%20Chen&owner=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "name": "Ava Chen",
  "owner": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/falai/latest/actions/flush-application-queue?${params}`, {
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
| `name` | string | yes | Serverless app name. |
| `owner` | string | yes | App owner name. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native fal.ai API returns.

## Native endpoint

Through the native fal.ai API, this operation is `DELETE /serverless/apps/:owner/:name/queue` (base URL `https://api.fal.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/flush-application-queue.md) for the provider-specific parameters and requirements.

