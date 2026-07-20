# Autype: Download Render Output File

Downloads a render output file from Autype.

```
GET https://connect.mindcloud.co/v1/universal/autype/latest/actions/download-render-output-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Autype `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/autype/latest/actions/download-render-output-file?connectionId=$CONNECTION_ID&jobId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "jobId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/autype/latest/actions/download-render-output-file?${params}`, {
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
| `jobId` | string | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Autype API returns.

## Native endpoint

Through the native Autype API, this operation is `GET /render/{jobId}/download` (base URL `https://api.autype.com/api/v1/dev`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/download-render-output-file.md) for the provider-specific parameters and requirements.

