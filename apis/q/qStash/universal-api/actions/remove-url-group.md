# QStash: Remove URL Group

Deletes a URL Group from QStash.

```
DELETE https://connect.mindcloud.co/v1/universal/qStash/latest/actions/remove-url-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a QStash `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/qStash/latest/actions/remove-url-group?connectionId=$CONNECTION_ID&urlGroupName=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "urlGroupName": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/qStash/latest/actions/remove-url-group?${params}`, {
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
| `urlGroupName` | string | yes | Name of the URL Group to remove. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native QStash API returns.

## Native endpoint

Through the native QStash API, this operation is `DELETE /v2/topics/:urlGroupName` (base URL `https://qstash-eu-central-1.upstash.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-url-group.md) for the provider-specific parameters and requirements.

