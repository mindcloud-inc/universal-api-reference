# Innform: Delete User

Deletes a user from Innform by ID or email.

```
DELETE https://connect.mindcloud.co/v1/universal/innform/latest/actions/delete-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Innform `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/innform/latest/actions/delete-user?connectionId=$CONNECTION_ID&idOrEmail=ava%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "idOrEmail": "ava@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/innform/latest/actions/delete-user?${params}`, {
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
| `idOrEmail` | string | yes | User UUID or email address. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Innform API returns.

## Native endpoint

Through the native Innform API, this operation is `DELETE /users/{idOrEmail}` (base URL `https://api.innform.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-user.md) for the provider-specific parameters and requirements.

