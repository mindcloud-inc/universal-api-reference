# Dropbox Sign: Get Template Files as File URL

Retrieves template files as file URLs from Dropbox Sign.

```
GET https://connect.mindcloud.co/v1/universal/dropboxSign/latest/actions/get-template-files-as-file-url
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dropbox Sign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dropboxSign/latest/actions/get-template-files-as-file-url?connectionId=$CONNECTION_ID&template_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "template_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dropboxSign/latest/actions/get-template-files-as-file-url?${params}`, {
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
| `force_download` | number | no | Set to 0 to display the PDF in the browser instead of downloading it. |
| `template_id` | string | yes | The ID of the template to retrieve files for. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "expiresAt": "2026-05-07T12:00:00.000Z",
      "fileUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `expiresAt` | date |  |
| `fileUrl` | string |  |

## Native endpoint

Through the native Dropbox Sign API, this operation is `GET /template/files_as_file_url/:template_id` (base URL `https://api.hellosign.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-template-files-as-file-url.md) for the provider-specific parameters and requirements.

