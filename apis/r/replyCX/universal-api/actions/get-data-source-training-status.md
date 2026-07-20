# ReplyCX: Get Data Source Training Status



```
GET https://connect.mindcloud.co/v1/universal/replyCX/latest/actions/get-data-source-training-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ReplyCX `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/replyCX/latest/actions/get-data-source-training-status?connectionId=$CONNECTION_ID&sourceIds=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "sourceIds": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/replyCX/latest/actions/get-data-source-training-status?${params}`, {
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
| `sourceIds` | string | yes | Comma-separated list of ReplyCX data source IDs. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native ReplyCX API returns.

## Native endpoint

Through the native ReplyCX API, this operation is `GET /api/v1/ai/status/sources` (base URL `https://api.reply.cx`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-data-source-training-status.md) for the provider-specific parameters and requirements.

