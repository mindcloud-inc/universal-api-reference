# Flatfile: Delete File

Deletes an existing file from Flatfile.

```
DELETE https://connect.mindcloud.co/v1/universal/flatfile/latest/actions/delete-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Flatfile `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/flatfile/latest/actions/delete-file?connectionId=$CONNECTION_ID&fileId=us_fil_mindcloud_flatfile" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "fileId": "us_fil_mindcloud_flatfile"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/flatfile/latest/actions/delete-file?${params}`, {
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
| `fileId` | string | yes | Flatfile file identifier. Default: `us_fil_mindcloud_flatfile`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean | Whether the delete succeeded. |

## Native endpoint

Through the native Flatfile API, this operation is `DELETE /files/:fileId` (base URL `https://api.x.flatfile.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-file.md) for the provider-specific parameters and requirements.

