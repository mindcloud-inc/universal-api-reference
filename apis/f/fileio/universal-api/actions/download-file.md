# File.io: Download File

Downloads a file from File.io by key.

```
GET https://connect.mindcloud.co/v1/universal/fileio/latest/actions/download-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a File.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fileio/latest/actions/download-file?connectionId=$CONNECTION_ID&key=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "key": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fileio/latest/actions/download-file?${params}`, {
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
| `key` | string | yes | File.io file key to download. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "file": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `file` | string | Raw downloaded file content returned by File.io. |

## Native endpoint

Through the native File.io API, this operation is `GET /{{key}}` (base URL `https://file.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/download-file.md) for the provider-specific parameters and requirements.

