# Zammad: Update Group

Updates an existing group in Zammad.

```
PUT https://connect.mindcloud.co/v1/universal/zammad/latest/actions/update-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zammad `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/zammad/latest/actions/update-group" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "3",
  "note": "MC TEST GROUP UPDATED"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zammad/latest/actions/update-group', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "3",
    "note": "MC TEST GROUP UPDATED"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | Group ID. Example: `3`. |
| `note` | string | yes | Group note. Example: `MC TEST GROUP UPDATED`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Zammad API returns.

## Native endpoint

Through the native Zammad API, this operation is `PUT /groups/:id` (base URL `{{credentials.baseUrl}}/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-group.md) for the provider-specific parameters and requirements.

