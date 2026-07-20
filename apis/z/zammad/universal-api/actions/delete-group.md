# Zammad: Delete Group

Deletes an existing group from Zammad.

```
DELETE https://connect.mindcloud.co/v1/universal/zammad/latest/actions/delete-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zammad `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/zammad/latest/actions/delete-group?connectionId=$CONNECTION_ID&id=3" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "3"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zammad/latest/actions/delete-group?${params}`, {
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
| `id` | number | yes | Group ID. Example: `3`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Zammad API returns.

## Native endpoint

Through the native Zammad API, this operation is `DELETE /groups/:id` (base URL `{{credentials.baseUrl}}/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-group.md) for the provider-specific parameters and requirements.

