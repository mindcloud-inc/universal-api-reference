# Documently: Delete Branch

Deletes an existing branch from Documently.

```
DELETE https://connect.mindcloud.co/v1/universal/documently/latest/actions/delete-branch
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Documently `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/documently/latest/actions/delete-branch?connectionId=$CONNECTION_ID&branchId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "branchId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/documently/latest/actions/delete-branch?${params}`, {
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
| `branchId` | string | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Documently API returns.

## Native endpoint

Through the native Documently API, this operation is `DELETE /branches/:branchId` (base URL `https://app.documently.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-branch.md) for the provider-specific parameters and requirements.

