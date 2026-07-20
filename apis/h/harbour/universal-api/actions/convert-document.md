# Harbour: Convert Document

Converts a Harbour document and returns a download URL.

```
GET https://connect.mindcloud.co/v1/universal/harbour/latest/actions/convert-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Harbour `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/harbour/latest/actions/convert-document?connectionId=$CONNECTION_ID&document_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "document_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/harbour/latest/actions/convert-document?${params}`, {
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
| `document_id` | string | yes | ID of the Harbour document to convert. |
| `format` | string | no | Target format. Harbour defaults to pdf. |
| `version_number` | number | no | Specific document version to convert. |

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

Through the native Harbour API, this operation is `POST /documents/:document_id/convert` (base URL `https://api.myharbourshare.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/convert-document.md) for the provider-specific parameters and requirements.

