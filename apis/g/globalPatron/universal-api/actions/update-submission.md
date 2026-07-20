# Global Patron: Update Submission

Updates a form submission in Global Patron.

```
PUT https://connect.mindcloud.co/v1/universal/globalPatron/latest/actions/update-submission
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Global Patron `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/globalPatron/latest/actions/update-submission" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "formId": "string",
  "submissionId": "string",
  "formFields[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/globalPatron/latest/actions/update-submission', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "formId": "string",
    "submissionId": "string",
    "formFields[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `formId` | string | yes | ID of the form. |
| `submissionId` | string | yes | ID of the submission to update. |
| `formFields[]` | array<object> | yes | Updated submission field values array from the GlobalPatron form definition. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "formSubmissionItemUpdated": true,
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `formSubmissionItemUpdated` | boolean | Whether the submission was updated. |
| `message` | string | Provider status message. |

## Native endpoint

Through the native Global Patron API, this operation is `POST /api/restricted/form/{formId}/submission/{submissionId}` (base URL `https://api.globalpatron.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-submission.md) for the provider-specific parameters and requirements.

