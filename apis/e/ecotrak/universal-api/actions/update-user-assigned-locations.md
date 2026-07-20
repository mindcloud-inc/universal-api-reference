# Ecotrak: Update User Assigned Locations

Updates a user's assigned locations in Ecotrak.

```
PUT https://connect.mindcloud.co/v1/universal/ecotrak/latest/actions/update-user-assigned-locations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ecotrak `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/ecotrak/latest/actions/update-user-assigned-locations" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "userId": 1,
  "orgIds[]": [
    1
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ecotrak/latest/actions/update-user-assigned-locations', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "userId": 1,
    "orgIds[]": [1]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `userId` | number | yes | Ecotrak user ID. |
| `orgIds[]` | array<number> | yes | Full list of assigned organization IDs. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Ecotrak API returns.

## Native endpoint

Through the native Ecotrak API, this operation is `PUT /v2/user/:user_id/location` (base URL `https://api.ecotrak.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-user-assigned-locations.md) for the provider-specific parameters and requirements.

