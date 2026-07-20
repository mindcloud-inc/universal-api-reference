# PDF-app: Update PDF Password

Updates a PDF password in PDF-app.

```
PUT https://connect.mindcloud.co/v1/universal/pDFApp/latest/actions/update-pdf-password
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PDF-app `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/pDFApp/latest/actions/update-pdf-password" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "fileUrl": "https://www.w3.org/WAI/ER/tests/xhtml/testfiles/resources/pdf/dummy.pdf"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pDFApp/latest/actions/update-pdf-password', {
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
| `fileUrl` | string | yes | PDF file URL to protect or unprotect. Example: `https://www.w3.org/WAI/ER/tests/xhtml/testfiles/resources/pdf/dummy.pdf`. |
| `passwordProtected` | string | no | Password to add or use when removing protection. Example: `mindcloud123`. |
| `fileName` | string | no | Desired output PDF file name. Example: `protected-dummy.pdf`. |
| `command` | string | no | Whether to addPassword or removePassword. Example: `addPassword`. |

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
| `creditsConsumed` | number | Credits consumed by the password update request. |
| `creditsRemaining` | number | Remaining provider credits after the password update request. |
| `job_id` | string | Provider job identifier for the password update request. |
| `message` | string | Summary of the PDF password update result. |
| `presignedUrl` | array<string> | Temporary download URLs for the updated PDF. |

## Native endpoint

Through the native PDF-app API, this operation is `POST /passwModPDFExt` (base URL `https://api.pdf-app.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-pdf-password.md) for the provider-specific parameters and requirements.

