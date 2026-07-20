# Harbour: Convert Document From Base64

Converts a base64 document in Harbour and returns a download URL.

```
GET https://connect.mindcloud.co/v1/universal/harbour/latest/actions/convert-document-from-base64
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Harbour `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/harbour/latest/actions/convert-document-from-base64?connectionId=$CONNECTION_ID&file_base64=string&filename=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "file_base64": "string",
  "filename": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/harbour/latest/actions/convert-document-from-base64?${params}`, {
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
| `file_base64` | string | yes | Base64 string for the source document file. |
| `filename` | string | yes | Original filename including extension. |
| `final_format` | string | no | Requested output format. Harbour defaults to pdf. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "download_url": "https://example.com",
      "expires_at": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `download_url` | string |  |
| `expires_at` | number |  |

## Native endpoint

Through the native Harbour API, this operation is `POST /documents/convert` (base URL `https://api.myharbourshare.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/convert-document-from-base64.md) for the provider-specific parameters and requirements.

