# Bytesafe: List Issues

Retrieves issues from your Bytesafe workspace.

```
GET https://connect.mindcloud.co/v1/universal/bytesafe/latest/actions/list-issues
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bytesafe `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bytesafe/latest/actions/list-issues?connectionId=$CONNECTION_ID&registry=string&status=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "registry": "string",
  "status": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bytesafe/latest/actions/list-issues?${params}`, {
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
| `registry` | string | yes | Registry ID or name to filter issues. |
| `status` | string | yes | Issue status to filter by. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Bytesafe API returns.

## Native endpoint

Through the native Bytesafe API, this operation is `GET /issues` (base URL `https://mindcloud.bytesafe.dev/api/v1/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-issues.md) for the provider-specific parameters and requirements.

