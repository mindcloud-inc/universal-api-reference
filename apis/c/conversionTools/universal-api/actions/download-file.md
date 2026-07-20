# Conversion Tools: Download File

Downloads a file from Conversion Tools.

```
GET https://connect.mindcloud.co/v1/universal/conversionTools/latest/actions/download-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Conversion Tools `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/conversionTools/latest/actions/download-file?connectionId=$CONNECTION_ID&fileId=b9bc512328764d5da56952ca39f82419" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "fileId": "b9bc512328764d5da56952ca39f82419"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/conversionTools/latest/actions/download-file?${params}`, {
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
| `fileId` | string | yes | The file ID returned by upload or task completion. Example: `b9bc512328764d5da56952ca39f82419`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Conversion Tools API returns.

## Native endpoint

Through the native Conversion Tools API, this operation is `GET /files/:fileId` (base URL `https://api.conversiontools.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/download-file.md) for the provider-specific parameters and requirements.

