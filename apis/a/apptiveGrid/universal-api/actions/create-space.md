# ApptiveGrid: Create Space

Creates a new space in ApptiveGrid.

```
POST https://connect.mindcloud.co/v1/universal/apptiveGrid/latest/actions/create-space
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ApptiveGrid `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/apptiveGrid/latest/actions/create-space" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "userId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/apptiveGrid/latest/actions/create-space', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "userId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | The space name. |
| `userId` | string | yes | The ApptiveGrid user id. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native ApptiveGrid API returns.

## Native endpoint

Through the native ApptiveGrid API, this operation is `POST /api/users/:user_id/spaces` (base URL `https://app.apptivegrid.de`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-space.md) for the provider-specific parameters and requirements.

