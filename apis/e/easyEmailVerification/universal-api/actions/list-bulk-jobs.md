# Easy Email Verification: List Bulk Jobs

Retrieves all bulk job statuses from Easy Email Verification.

```
GET https://connect.mindcloud.co/v1/universal/easyEmailVerification/latest/actions/list-bulk-jobs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Easy Email Verification `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/easyEmailVerification/latest/actions/list-bulk-jobs?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/easyEmailVerification/latest/actions/list-bulk-jobs?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Easy Email Verification API returns.

## Native endpoint

Through the native Easy Email Verification API, this operation is `GET /bulk/status` (base URL `https://api.easyemailverification.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-bulk-jobs.md) for the provider-specific parameters and requirements.

