# Sender: Rename Group



```
PUT https://connect.mindcloud.co/v1/universal/sender/latest/actions/rename-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sender `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/sender/latest/actions/rename-group" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "grp_123"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sender/latest/actions/rename-group', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "grp_123"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Group ID. Example: `grp_123`. |
| `title` | string | no | Provide a different name for this group. Example: `Spring Launch`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string | Success message returned when a Sender group is renamed. |

## Native endpoint

Through the native Sender API, this operation is `PATCH /groups/:id` (base URL `https://api.sender.net/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/rename-group.md) for the provider-specific parameters and requirements.

