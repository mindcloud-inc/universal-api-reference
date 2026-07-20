# Merge: Get CRM Account



```
GET https://connect.mindcloud.co/v1/universal/merge/latest/actions/get-crm-account
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Merge `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/merge/latest/actions/get-crm-account?connectionId=$CONNECTION_ID&accountToken=linked-account-token&id=merge-object-id" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "accountToken": "linked-account-token",
  "id": "merge-object-id"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/merge/latest/actions/get-crm-account?${params}`, {
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
| `id` | string | yes | Merge object ID. Example: `merge-object-id`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Merge API returns.

## Native endpoint

Through the native Merge API, this operation is `GET /api/crm/v1/accounts/{id}` (base URL `https://api.merge.dev`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-crm-account.md) for the provider-specific parameters and requirements.

