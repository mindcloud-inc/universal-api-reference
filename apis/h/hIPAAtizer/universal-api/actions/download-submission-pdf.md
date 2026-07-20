# HIPAAtizer: Download Submission PDF

Retrieves a submission PDF from HIPAAtizer.

```
GET https://connect.mindcloud.co/v1/universal/hIPAAtizer/latest/actions/download-submission-pdf
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HIPAAtizer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hIPAAtizer/latest/actions/download-submission-pdf?connectionId=$CONNECTION_ID&submissionId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "submissionId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hIPAAtizer/latest/actions/download-submission-pdf?${params}`, {
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
| `submissionId` | string | yes | Submission identifier. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fileOrder` | number | no | Optional file order index for PDF generation. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "file": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `file` | string |  |

## Native endpoint

Through the native HIPAAtizer API, this operation is `GET /api/v1/api_key/submissions/:submissionId/pdf` (base URL `https://app.hipaatizer.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/download-submission-pdf.md) for the provider-specific parameters and requirements.

