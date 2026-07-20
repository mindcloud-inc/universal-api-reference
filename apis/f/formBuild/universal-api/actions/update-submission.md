# 123FormBuild: Update Submission

Updates an existing submission in a 123FormBuilder form.

```
PUT https://connect.mindcloud.co/v1/universal/formBuild/latest/actions/update-submission
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 123FormBuild `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/formBuild/latest/actions/update-submission" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "formId": 1,
  "submissionId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/formBuild/latest/actions/update-submission', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "formId": 1,
    "submissionId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `formId` | number | yes | The ID of the form |
| `submissionId` | number | yes | The ID of the submission |
| `payed` | string | no | Payment status for the submission |
| `approved` | number | no | Approval status for the submission |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native 123FormBuild API returns.

## Native endpoint

Through the native 123FormBuild API, this operation is `PUT /forms/{form_id}/submissions/{submission_id}` (base URL `https://api.123formbuilder.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-submission.md) for the provider-specific parameters and requirements.

