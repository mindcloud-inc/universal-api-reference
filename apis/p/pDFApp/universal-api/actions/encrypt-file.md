# PDF-app: Encrypt File

Updates a file with password encryption in PDF-app.

```
PUT https://connect.mindcloud.co/v1/universal/pDFApp/latest/actions/encrypt-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PDF-app `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/pDFApp/latest/actions/encrypt-file" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "fileUrl": "https://www.w3.org/WAI/ER/tests/xhtml/testfiles/resources/pdf/dummy.pdf"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pDFApp/latest/actions/encrypt-file', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "fileUrl": "https://www.w3.org/WAI/ER/tests/xhtml/testfiles/resources/pdf/dummy.pdf"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fileUrl` | string | yes | File URL to encrypt or decrypt. Example: `https://www.w3.org/WAI/ER/tests/xhtml/testfiles/resources/pdf/dummy.pdf`. |
| `selfEncrypt` | object | no | Encryption settings including algorithm, key, and IV. Runtime verification confirmed `aes256`/`AES256` as accepted algorithm tokens. Example: `[object Object]`. |
| `fileName` | string | no | Desired output file name. Example: `encrypted-dummy`. |
| `command` | string | no | Whether to encrypt or decrypt the file. Example: `encrypt`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "creditsConsumed": 1,
      "creditsRemaining": 1,
      "job_id": "string",
      "message": "string",
      "presignedUrl": [
        "https://example.com"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `creditsConsumed` | number | Credits consumed by the operation |
| `creditsRemaining` | number | Remaining account credits after the run |
| `job_id` | string | Processing job identifier |
| `message` | string | Provider success message |
| `presignedUrl` | array<string> | Temporary download URLs for the encrypted file |

## Native endpoint

Through the native PDF-app API, this operation is `POST /encryptFileExt` (base URL `https://api.pdf-app.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/encrypt-file.md) for the provider-specific parameters and requirements.

