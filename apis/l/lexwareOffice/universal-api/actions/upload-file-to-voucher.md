# Lexware Office: Upload File to Voucher

Uploads a file to a voucher in Lexware Office.

```
POST https://connect.mindcloud.co/v1/universal/lexwareOffice/latest/actions/upload-file-to-voucher
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lexware Office `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/lexwareOffice/latest/actions/upload-file-to-voucher" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "780a9985-29a1-4daa-aa9c-196ee0dd99f5",
  "file": "<base64-or-buffer>"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/lexwareOffice/latest/actions/upload-file-to-voucher', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "780a9985-29a1-4daa-aa9c-196ee0dd99f5",
    "file": "<base64-or-buffer>"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Voucher ID from Lexware. Example: `780a9985-29a1-4daa-aa9c-196ee0dd99f5`. |
| `file` | file | yes | PDF, image, or XML file content to attach. Example: `<base64-or-buffer>`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Attachment ID created for the voucher upload. |

## Native endpoint

Through the native Lexware Office API, this operation is `POST /v1/vouchers/:id/files` (base URL `https://api.lexware.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-file-to-voucher.md) for the provider-specific parameters and requirements.

