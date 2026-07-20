# Reach360: Add User To Group

Adds a user to a Reach360 group.

```
POST https://connect.mindcloud.co/v1/universal/reach360/latest/actions/add-user-to-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reach360 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/reach360/latest/actions/add-user-to-group" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "groupId": "string",
  "userId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/reach360/latest/actions/add-user-to-group', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "groupId": "string",
    "userId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `groupId` | string | yes | The group ID. |
| `userId` | string | yes | The user ID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Reach360 API returns.

## Native endpoint

Through the native Reach360 API, this operation is `PUT /groups/:groupId/users/:userId` (base URL `https://api.reach360.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-user-to-group.md) for the provider-specific parameters and requirements.

