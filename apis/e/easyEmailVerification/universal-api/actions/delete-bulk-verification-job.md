# Easy Email Verification: Delete Bulk Verification Job

Deletes a bulk verification job from Easy Email Verification.

```
DELETE https://connect.mindcloud.co/v1/universal/easyEmailVerification/latest/actions/delete-bulk-verification-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Easy Email Verification `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/easyEmailVerification/latest/actions/delete-bulk-verification-job?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/easyEmailVerification/latest/actions/delete-bulk-verification-job?${params}`, {
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
| `id` | string | yes | Bulk verification job ID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Easy Email Verification API returns.

## Native endpoint

Through the native Easy Email Verification API, this operation is `DELETE /bulk/:id` (base URL `https://api.easyemailverification.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-bulk-verification-job.md) for the provider-specific parameters and requirements.

