# Formstack: Get Submission Upload

Retrieves an uploaded file from a Formstack submission.

```
GET https://connect.mindcloud.co/v1/universal/formstack/latest/actions/get-submission-upload
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Formstack `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/formstack/latest/actions/get-submission-upload?connectionId=$CONNECTION_ID&submissionId=1&fieldId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "submissionId": "1",
  "fieldId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/formstack/latest/actions/get-submission-upload?${params}`, {
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
| `submissionId` | number | yes | The unique identifier of the submission containing the upload. |
| `fieldId` | number | yes | The unique identifier of the field containing the uploaded file. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `index` | number | no | The zero-based index of the file when a field contains multiple uploads. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        1
      ],
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data[]` | number | Binary file bytes represented as an array of numeric byte values. |
| `type` | string | Raw response marker emitted by the runtime for binary download payloads. |

## Native endpoint

Through the native Formstack API, this operation is `GET /submissions/:submissionId/upload` (base URL `https://www.formstack.com/api/v2025`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-submission-upload.md) for the provider-specific parameters and requirements.

