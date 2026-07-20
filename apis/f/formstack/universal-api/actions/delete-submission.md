# Formstack: Delete Submission

Permanently deletes a submission and its associated data from Formstack.

```
DELETE https://connect.mindcloud.co/v1/universal/formstack/latest/actions/delete-submission
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Formstack `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/formstack/latest/actions/delete-submission?connectionId=$CONNECTION_ID&submissionId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "submissionId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/formstack/latest/actions/delete-submission?${params}`, {
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
| `submissionId` | number | yes | The unique identifier of the submission to delete. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number | The ID of the deleted submission. |

## Native endpoint

Through the native Formstack API, this operation is `DELETE /submissions/:submissionId` (base URL `https://www.formstack.com/api/v2025`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-submission.md) for the provider-specific parameters and requirements.

