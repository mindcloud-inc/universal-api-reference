# QStash: Remove URL Group Endpoints

Removes endpoints from a QStash URL Group.

```
DELETE https://connect.mindcloud.co/v1/universal/qStash/latest/actions/remove-url-group-endpoints
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a QStash `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/qStash/latest/actions/remove-url-group-endpoints?connectionId=$CONNECTION_ID&urlGroupName=https%3A%2F%2Fexample.com&endpoints%5B%5D=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "urlGroupName": "https://example.com",
  "endpoints[]": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/qStash/latest/actions/remove-url-group-endpoints?${params}`, {
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
| `urlGroupName` | string | yes | Name of the URL Group. |
| `endpoints[]` | array<object> | yes | Endpoints to remove from the URL Group. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native QStash API returns.

## Native endpoint

Through the native QStash API, this operation is `DELETE /v2/topics/:urlGroupName/endpoints` (base URL `https://qstash-eu-central-1.upstash.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-url-group-endpoints.md) for the provider-specific parameters and requirements.

