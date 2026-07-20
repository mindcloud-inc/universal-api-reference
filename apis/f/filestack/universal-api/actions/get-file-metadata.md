# Filestack: Get File Metadata

Retrieves file metadata from Filestack.

```
GET https://connect.mindcloud.co/v1/universal/filestack/latest/actions/get-file-metadata
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Filestack `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/filestack/latest/actions/get-file-metadata?connectionId=$CONNECTION_ID&handle=DCL5K46FS3OIxb5iuKby" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "handle": "DCL5K46FS3OIxb5iuKby"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/filestack/latest/actions/get-file-metadata?${params}`, {
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
| `handle` | string | yes | The Filestack file handle, for example itnd50g6QzehEsWjDGij. Default: `zJKAH3U9SP60pyZnyrp4`. Example: `DCL5K46FS3OIxb5iuKby`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "filename": "Ava Chen",
      "mimetype": "string",
      "size": 1,
      "uploaded": 1,
      "writeable": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `filename` | string | The filename returned by Filestack metadata. |
| `mimetype` | string | The file MIME type returned by Filestack metadata. |
| `size` | number | The file size in bytes. |
| `uploaded` | number | Timestamp when the file was uploaded. |
| `writeable` | boolean | Whether the file is writeable. |

## Native endpoint

Through the native Filestack API, this operation is `GET /file/:handle/metadata` (base URL `https://www.filestackapi.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-file-metadata.md) for the provider-specific parameters and requirements.

