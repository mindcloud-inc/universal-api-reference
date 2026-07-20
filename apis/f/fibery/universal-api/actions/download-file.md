# Fibery: Download File

Retrieves a file from Fibery.

```
GET https://connect.mindcloud.co/v1/universal/fibery/latest/actions/download-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fibery `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fibery/latest/actions/download-file?connectionId=$CONNECTION_ID&secret=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "secret": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fibery/latest/actions/download-file?${params}`, {
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
| `secret` | string | yes | File secret used in /api/files/:secret. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Fibery API returns.

## Native endpoint

Through the native Fibery API, this operation is `GET /files/:secret` (base URL `https://{{credentials.account}}.fibery.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/download-file.md) for the provider-specific parameters and requirements.

