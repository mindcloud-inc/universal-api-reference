# Meisterplan: Delete Role

Deletes an existing role from Meisterplan.

```
DELETE https://connect.mindcloud.co/v1/universal/meisterplan/latest/actions/delete-role
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Meisterplan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/meisterplan/latest/actions/delete-role?connectionId=$CONNECTION_ID&roleId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "roleId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/meisterplan/latest/actions/delete-role?${params}`, {
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
| `roleId` | string | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Meisterplan API returns.

## Native endpoint

Through the native Meisterplan API, this operation is `DELETE /roles/:roleId` (base URL `https://api.us.meisterplan.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-role.md) for the provider-specific parameters and requirements.

