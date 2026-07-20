# Global Patron: Retrieve Submission Attachment

Retrieves a submission attachment download link from Global Patron.

```
GET https://connect.mindcloud.co/v1/universal/globalPatron/latest/actions/retrieve-submission-attachment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Global Patron `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/globalPatron/latest/actions/retrieve-submission-attachment?connectionId=$CONNECTION_ID&formId=string&attachmentId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "formId": "string",
  "attachmentId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/globalPatron/latest/actions/retrieve-submission-attachment?${params}`, {
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
| `formId` | string | yes | ID of the form. |
| `attachmentId` | string | yes | ID of the submission attachment. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attachmentSasUri": "string",
      "contentType": "string",
      "fileSize": 1,
      "formId": "string",
      "id": "string",
      "submissionId": "string",
      "unsafeOriginalFilename": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attachmentSasUri` | string | Temporary attachment access URL. |
| `contentType` | string | Attachment MIME type. |
| `fileSize` | number | Attachment size in bytes. |
| `formId` | string | Form identifier for the attachment. |
| `id` | string | Attachment identifier. |
| `submissionId` | string | Submission identifier when returned. |
| `unsafeOriginalFilename` | string | Original uploaded filename. |

## Native endpoint

Through the native Global Patron API, this operation is `GET /api/restricted/form/{formId}/submissionattachment/{attachmentId}` (base URL `https://api.globalpatron.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-submission-attachment.md) for the provider-specific parameters and requirements.

