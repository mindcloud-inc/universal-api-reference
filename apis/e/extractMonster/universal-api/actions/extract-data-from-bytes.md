# Extract Monster: Extract Data From Bytes

Extracts structured data from file bytes in Extract Monster.

```
GET https://connect.mindcloud.co/v1/universal/extractMonster/latest/actions/extract-data-from-bytes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Extract Monster `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/extractMonster/latest/actions/extract-data-from-bytes?connectionId=$CONNECTION_ID&fileBytes=Paste%20base64-encoded%20file%20content.&filename=example.pdf" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "fileBytes": "Paste base64-encoded file content.",
  "filename": "example.pdf"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/extractMonster/latest/actions/extract-data-from-bytes?${params}`, {
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
| `fileBytes` | string | yes | Base64-encoded file content. Example: `Paste base64-encoded file content.`. |
| `filename` | string | yes | Original filename with extension. Example: `example.pdf`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "extractedData": {},
      "filename": "Ava Chen",
      "fileSize": 1,
      "fileType": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `extractedData` | object | Structured extraction payload returned for the byte input. |
| `filename` | string | Submitted file name. |
| `fileSize` | number | Decoded input size in bytes. |
| `fileType` | string | Detected file/media type. |
| `status` | string | Extraction request status. |

## Native endpoint

Through the native Extract Monster API, this operation is `POST /v1/extract/bytes` (base URL `https://api.extract.monster`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/extract-data-from-bytes.md) for the provider-specific parameters and requirements.

