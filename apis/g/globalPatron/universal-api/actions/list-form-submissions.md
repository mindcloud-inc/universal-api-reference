# Global Patron: List Form Submissions

Lists form submissions in Global Patron.

```
GET https://connect.mindcloud.co/v1/universal/globalPatron/latest/actions/list-form-submissions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Global Patron `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/globalPatron/latest/actions/list-form-submissions?connectionId=$CONNECTION_ID&formId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "formId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/globalPatron/latest/actions/list-form-submissions?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `includeFormDefinition` | boolean | no | Include form definition in the submissions response. |
| `dateFrom` | date | no | Start date for submission filtering. |
| `dateTo` | date | no | End date for submission filtering. |
| `batchSize` | number | no | Number of submissions to return in a batch. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "formDefinition": {},
      "grantedFormRoles": [
        "string"
      ],
      "results": [
        {
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
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `formDefinition` | object | Form definition returned when requested. |
| `grantedFormRoles` | array<string> | Roles granted to the current user. |
| `results` | array<object> | Submission records for the form. |
| `results[].createdDateUtc` | date | Submission creation timestamp. |
| `results[].formFields` | array<object> | Submitted form fields. |
| `results[].formFields[].submittedValue` | string | Submitted field value. |
| `results[].formFields[].uniqueSystemName` | string | Form field system name. |
| `results[].formId` | string | Form identifier. |
| `results[].id` | string | Submission identifier. |
| `results[].isDraftSubmission` | boolean | Whether the submission is a draft. |
| `results[].modifiedDateUtc` | date | Submission modification timestamp. |
| `results[].staleFormName` | string | Form name stored on the submission. |

## Native endpoint

Through the native Global Patron API, this operation is `GET /api/restricted/form/{formId}/submissions` (base URL `https://api.globalpatron.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-form-submissions.md) for the provider-specific parameters and requirements.

