# Pencil Spaces: Create Space



```
POST https://connect.mindcloud.co/v1/universal/pencilSpaces/latest/actions/create-space
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pencil Spaces `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pencilSpaces/latest/actions/create-space" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "notifyInvitees": true
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pencilSpaces/latest/actions/create-space', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "notifyInvitees": true
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `externalId` | string | no | Unique external identifier for the Space. |
| `notifyInvitees` | boolean | yes | Whether invitees should be notified when the Space is created. |
| `title` | string | no | The title of the Space. |
| `visibility` | string | no | Default visibility for the Space. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Pencil Spaces API returns.

## Native endpoint

Through the native Pencil Spaces API, this operation is `POST /spaces/create` (base URL `https://apis.pencilapp.com/public/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-space.md) for the provider-specific parameters and requirements.

