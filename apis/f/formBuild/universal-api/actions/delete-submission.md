# 123FormBuild: Delete Submission

Deletes an existing submission from a 123FormBuilder form.

```
DELETE https://connect.mindcloud.co/v1/universal/formBuild/latest/actions/delete-submission
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 123FormBuild `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/formBuild/latest/actions/delete-submission?connectionId=$CONNECTION_ID&formId=1&submissionId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "formId": "1",
  "submissionId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/formBuild/latest/actions/delete-submission?${params}`, {
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
| `formId` | number | yes | The ID of the form |
| `submissionId` | number | yes | The ID of the submission |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native 123FormBuild API returns.

## Native endpoint

Through the native 123FormBuild API, this operation is `DELETE /forms/{form_id}/submissions/{submission_id}` (base URL `https://api.123formbuilder.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-submission.md) for the provider-specific parameters and requirements.

