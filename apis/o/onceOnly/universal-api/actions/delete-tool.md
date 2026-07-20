# OnceOnly: Delete Tool

Deletes a tool from OnceOnly.

```
DELETE https://connect.mindcloud.co/v1/universal/onceOnly/latest/actions/delete-tool
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OnceOnly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/onceOnly/latest/actions/delete-tool?connectionId=$CONNECTION_ID&name=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "name": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/onceOnly/latest/actions/delete-tool?${params}`, {
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
| `name` | string | yes | Tool name. |
| `scopeId` | string | no | Tool scope. Default: `global`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native OnceOnly API returns.

## Native endpoint

Through the native OnceOnly API, this operation is `DELETE /v1/tools/:name` (base URL `https://api.onceonly.tech`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-tool.md) for the provider-specific parameters and requirements.

