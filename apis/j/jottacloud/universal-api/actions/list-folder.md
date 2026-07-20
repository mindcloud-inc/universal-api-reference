# Jottacloud: List Folder



```
GET https://connect.mindcloud.co/v1/universal/jottacloud/latest/actions/list-folder
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Jottacloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/jottacloud/latest/actions/list-folder?connectionId=$CONNECTION_ID&path=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "path": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/jottacloud/latest/actions/list-folder?${params}`, {
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
| `path` | string | yes | Logical folder path such as Archive or /Archive/folder. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Jottacloud API returns.

## Native endpoint

Through the native Jottacloud API, this operation is `POST /files/v2/list_folder` (base URL `https://api.jotta.cloud`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-folder.md) for the provider-specific parameters and requirements.

