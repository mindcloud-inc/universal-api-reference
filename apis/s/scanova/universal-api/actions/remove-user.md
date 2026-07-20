# Scanova: Remove User



```
DELETE https://connect.mindcloud.co/v1/universal/scanova/latest/actions/remove-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Scanova `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/scanova/latest/actions/remove-user?connectionId=$CONNECTION_ID&sharedUserId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "sharedUserId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scanova/latest/actions/remove-user?${params}`, {
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
| `sharedUserId` | number | yes | ID of the shared user to remove |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Scanova API returns.

## Native endpoint

Through the native Scanova API, this operation is `DELETE /multi-users/{shared-user-id}/` (base URL `https://management.scanova.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-user.md) for the provider-specific parameters and requirements.

