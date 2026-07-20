# Zammad: Update Role

Updates an existing role in Zammad.

```
PUT https://connect.mindcloud.co/v1/universal/zammad/latest/actions/update-role
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zammad `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/zammad/latest/actions/update-role" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "5",
  "note": "MC TEST ROLE UPDATED"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zammad/latest/actions/update-role', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "5",
    "note": "MC TEST ROLE UPDATED"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | Role ID. Example: `5`. |
| `note` | string | yes | Role note. Example: `MC TEST ROLE UPDATED`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Zammad API returns.

## Native endpoint

Through the native Zammad API, this operation is `PUT /roles/:id` (base URL `{{credentials.baseUrl}}/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-role.md) for the provider-specific parameters and requirements.

