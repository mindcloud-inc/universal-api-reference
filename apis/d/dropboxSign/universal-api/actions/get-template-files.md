# Dropbox Sign: Get Template Files

Retrieves template files from Dropbox Sign.

```
GET https://connect.mindcloud.co/v1/universal/dropboxSign/latest/actions/get-template-files
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dropbox Sign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dropboxSign/latest/actions/get-template-files?connectionId=$CONNECTION_ID&template_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "template_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dropboxSign/latest/actions/get-template-files?${params}`, {
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
| `fileType` | string | no | Set to pdf for a single merged document or zip for a collection of individual documents. |
| `template_id` | string | yes | The ID of the template to retrieve files for. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "response": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `response` | string | Raw PDF binary content returned by Dropbox Sign. |

## Native endpoint

Through the native Dropbox Sign API, this operation is `GET /template/files/:template_id` (base URL `https://api.hellosign.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-template-files.md) for the provider-specific parameters and requirements.

