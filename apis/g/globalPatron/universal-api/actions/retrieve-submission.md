# Global Patron: Retrieve Submission

Retrieves a form submission from Global Patron.

```
GET https://connect.mindcloud.co/v1/universal/globalPatron/latest/actions/retrieve-submission
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Global Patron `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/globalPatron/latest/actions/retrieve-submission?connectionId=$CONNECTION_ID&formId=string&submissionId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "formId": "string",
  "submissionId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/globalPatron/latest/actions/retrieve-submission?${params}`, {
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
| `submissionId` | string | yes | ID of the submission. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attachmentDetails": [
        {
          "attachment": {
            "fileSize": 1,
            "formId": "string",
            "id": "string",
            "unsafeOriginalFilename": "Ava Chen"
          },
          "attachmentSasUri": "string"
        }
      ],
      "formSubmission": {
        "createdDateUtc": "2026-05-07T12:00:00.000Z",
        "formFields": [
          {
            "submittedValue": "string",
            "uniqueSystemName": "Ava Chen"
          }
        ],
        "formId": "string",
        "id": "string",
        "isDraftSubmission": true,
        "modifiedDateUtc": "2026-05-07T12:00:00.000Z",
        "staleFormName": "Ava Chen"
      },
      "userHasEditSubmissionAccess": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attachmentDetails` | array<object> | Attachment metadata and temporary links. |
| `attachmentDetails[].attachment` | object | Attachment record. |
| `attachmentDetails[].attachment.fileSize` | number | Attachment size in bytes. |
| `attachmentDetails[].attachment.formId` | string | Form identifier for the attachment. |
| `attachmentDetails[].attachment.id` | string | Attachment identifier. |
| `attachmentDetails[].attachment.unsafeOriginalFilename` | string | Original uploaded filename. |
| `attachmentDetails[].attachmentSasUri` | string | Temporary attachment access URL. |
| `formSubmission` | object | Retrieved form submission. |
| `formSubmission.createdDateUtc` | date | Submission creation timestamp. |
| `formSubmission.formFields` | array<object> | Submitted form fields. |
| `formSubmission.formFields[].submittedValue` | string | Submitted field value. |
| `formSubmission.formFields[].uniqueSystemName` | string | Form field system name. |
| `formSubmission.formId` | string | Form identifier. |
| `formSubmission.id` | string | Submission identifier. |
| `formSubmission.isDraftSubmission` | boolean | Whether the submission is a draft. |
| `formSubmission.modifiedDateUtc` | date | Submission modification timestamp. |
| `formSubmission.staleFormName` | string | Form name stored on the submission. |
| `userHasEditSubmissionAccess` | boolean | Whether the current user can edit the submission. |

## Native endpoint

Through the native Global Patron API, this operation is `GET /api/restricted/form/{formId}/submission/{submissionId}` (base URL `https://api.globalpatron.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-submission.md) for the provider-specific parameters and requirements.

