# Tolq: Initiate File Upload

Initiates a file upload in Tolq.

```
POST https://connect.mindcloud.co/v1/universal/tolq/latest/actions/initiate-file-upload
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tolq `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/tolq/latest/actions/initiate-file-upload" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "file_name": "mindcloud-upload-validation.csv",
  "source_language_code": "en"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/tolq/latest/actions/initiate-file-upload', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "file_name": "mindcloud-upload-validation.csv",
    "source_language_code": "en"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `file_name` | string | yes | File name including supported extension such as csv, html, json, or xml. Example: `mindcloud-upload-validation.csv`. |
| `source_language_code` | string | yes | Two-letter ISO 639-1 source language code. Example: `en`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `separator` | string | no | Optional separator character for csv files. Example: `,`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "name": "Ava Chen",
      "s3_url": "https://example.com",
      "uid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `name` | string |  |
| `s3_url` | string |  |
| `uid` | string |  |

## Native endpoint

Through the native Tolq API, this operation is `POST /translations/requests/upload` (base URL `https://api.tolq.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/initiate-file-upload.md) for the provider-specific parameters and requirements.

