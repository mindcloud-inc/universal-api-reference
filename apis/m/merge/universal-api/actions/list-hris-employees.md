# Merge: List HRIS Employees



```
GET https://connect.mindcloud.co/v1/universal/merge/latest/actions/list-hris-employees
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Merge `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/merge/latest/actions/list-hris-employees?connectionId=$CONNECTION_ID&limit=25&offset=0&accountToken=linked-account-token" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "accountToken": "linked-account-token"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/merge/latest/actions/list-hris-employees?${params}`, {
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
| `accountToken` | string | yes | Linked account token for the Merge account you want to query. The shared headers mapper sends this input as X-Account-Token. Example: `linked-account-token`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Merge API returns.

## Native endpoint

Through the native Merge API, this operation is `GET /api/hris/v1/employees` (base URL `https://api.merge.dev`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-hris-employees.md) for the provider-specific parameters and requirements.

