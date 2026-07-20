# PDF.co: Get PDF Form Fields Info

Retrieves PDF form field info from PDF.co.

```
GET https://connect.mindcloud.co/v1/universal/pDFco/latest/actions/get-pdf-form-fields-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PDF.co `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pDFco/latest/actions/get-pdf-form-fields-info?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fpdfco-test-files.s3.us-west-2.amazonaws.com%2Fpdf-form-fields%2Fform.pdf" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "https://pdfco-test-files.s3.us-west-2.amazonaws.com/pdf-form-fields/form.pdf"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pDFco/latest/actions/get-pdf-form-fields-info?${params}`, {
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
| `url` | string | yes | Source PDF URL. Example: `https://pdfco-test-files.s3.us-west-2.amazonaws.com/pdf-form-fields/form.pdf`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `password` | string | no | Password for protected PDF. Example: `your-password`. |
| `async` | boolean | no | Set true to run as async job. Example: `false`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "credits": 1,
      "duration": 1,
      "error": true,
      "info": {},
      "remainingCredits": 1,
      "status": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `credits` | number |  |
| `duration` | number |  |
| `error` | boolean |  |
| `info` | object |  |
| `remainingCredits` | number |  |
| `status` | number |  |

## Native endpoint

Through the native PDF.co API, this operation is `POST /pdf/info/fields` (base URL `https://api.pdf.co/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-pdf-form-fields-info.md) for the provider-specific parameters and requirements.

