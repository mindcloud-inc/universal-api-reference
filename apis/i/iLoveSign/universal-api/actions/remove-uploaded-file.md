# iLoveSign: Remove Uploaded File



```
DELETE https://connect.mindcloud.co/v1/universal/iLoveSign/latest/actions/remove-uploaded-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a iLoveSign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/iLoveSign/latest/actions/remove-uploaded-file?connectionId=$CONNECTION_ID&server=api11.ilovepdf.com&task=string&serverFilename=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "server": "api11.ilovepdf.com",
  "task": "string",
  "serverFilename": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/iLoveSign/latest/actions/remove-uploaded-file?${params}`, {
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
| `server` | string | yes | Task-assigned host returned by the start call. Example: `api11.ilovepdf.com`. |
| `task` | string | yes | Task identifier that owns the uploaded file. |
| `serverFilename` | string | yes | Uploaded server filename to remove from the task. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native iLoveSign API returns.

## Native endpoint

Through the native iLoveSign API, this operation is `DELETE https://:server/v1/upload/:task/:server_filename` (base URL `https://api.ilovepdf.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-uploaded-file.md) for the provider-specific parameters and requirements.

