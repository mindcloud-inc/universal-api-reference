# MyEmailVerifier: Upload Verification File

Creates a bulk verification upload in MyEmailVerifier.

```
POST https://connect.mindcloud.co/v1/universal/myEmailVerifier/latest/actions/upload-verification-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MyEmailVerifier `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/myEmailVerifier/latest/actions/upload-verification-file" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "filename": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/myEmailVerifier/latest/actions/upload-verification-file', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "filename": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `filename` | file | yes | Required TXT, CSV, or XLSX file containing one email address per row. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "file_id": 1,
      "file_name": "Ava Chen",
      "message": "string",
      "status": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Upload metadata including line count and remaining credits. |
| `file_id` | number | Bulk verification file identifier for follow-up status checks. |
| `file_name` | string | Original uploaded file name. |
| `message` | string | Provider message about the upload result. |
| `status` | boolean | Whether the upload request succeeded. |

## Native endpoint

Through the native MyEmailVerifier API, this operation is `POST /verifier/upload_file` (base URL `https://client.myemailverifier.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-verification-file.md) for the provider-specific parameters and requirements.

