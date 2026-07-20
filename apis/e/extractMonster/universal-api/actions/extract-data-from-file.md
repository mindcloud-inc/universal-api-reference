# Extract Monster: Extract Data From File

Extracts structured data from a file in Extract Monster.

```
GET https://connect.mindcloud.co/v1/universal/extractMonster/latest/actions/extract-data-from-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Extract Monster `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/extractMonster/latest/actions/extract-data-from-file?connectionId=$CONNECTION_ID&file=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "file": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/extractMonster/latest/actions/extract-data-from-file?${params}`, {
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
| `file` | file | yes | File to upload for structured data extraction. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `jsonSchema` | string | no | Optional JSON schema string used to structure the extracted output. Example: `Optional JSON schema string.`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "extractedData": {},
      "filename": "Ava Chen",
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
| `extractedData` | object | Structured extraction payload returned for the uploaded file. |
| `filename` | string | Uploaded file name. |
| `fileType` | string | Detected file/media type. |
| `status` | string | Extraction request status. |

## Native endpoint

Through the native Extract Monster API, this operation is `POST /v1/extract/file` (base URL `https://api.extract.monster`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/extract-data-from-file.md) for the provider-specific parameters and requirements.

