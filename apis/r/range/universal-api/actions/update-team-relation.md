# Range: Update Team Relation

Update the relationship between a team and user.

```
PUT https://connect.mindcloud.co/v1/universal/range/latest/actions/update-team-relation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Range `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/range/latest/actions/update-team-relation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/range/latest/actions/update-team-relation', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `teamId` | string | no | The team ID to update. |
| `userId` | string | no | The user ID to relate to the team. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "isMember": true,
      "receiveUpdates": true,
      "role": "string",
      "teamId": "string",
      "updatedAt": "string",
      "userId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string |  |
| `isMember` | boolean |  |
| `receiveUpdates` | boolean |  |
| `role` | string |  |
| `teamId` | string |  |
| `updatedAt` | string |  |
| `userId` | string |  |

## Native endpoint

Through the native Range API, this operation is `PUT /v1/teams/:teamId/relations/:userId` (base URL `https://api.range.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-team-relation.md) for the provider-specific parameters and requirements.

