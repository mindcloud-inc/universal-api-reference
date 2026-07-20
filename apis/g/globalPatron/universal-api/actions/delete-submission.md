# Global Patron: Delete Submission

Deletes a form submission from Global Patron.

```
DELETE https://connect.mindcloud.co/v1/universal/globalPatron/latest/actions/delete-submission
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Global Patron `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/globalPatron/latest/actions/delete-submission?connectionId=$CONNECTION_ID&formId=string&submissionId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "formId": "string",
  "submissionId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/globalPatron/latest/actions/delete-submission?${params}`, {
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
| `submissionId` | string | yes | ID of the submission to delete. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "formSubmissionItemDeleted": true,
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `formSubmissionItemDeleted` | boolean | Whether the submission was deleted. |
| `message` | string | Provider status message. |

## Native endpoint

Through the native Global Patron API, this operation is `DELETE /api/restricted/form/{formId}/submission/{submissionId}` (base URL `https://api.globalpatron.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-submission.md) for the provider-specific parameters and requirements.

