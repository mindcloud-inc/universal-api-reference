# Asset Panda: Create Group Action

Creates a new group action in Asset Panda.

```
POST https://connect.mindcloud.co/v1/universal/assetPanda/latest/actions/create-group-action
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Asset Panda `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/assetPanda/latest/actions/create-group-action" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/assetPanda/latest/actions/create-group-action', {
  method: 'POST',
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
| `groupId` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Asset Panda API returns.

## Native endpoint

Through the native Asset Panda API, this operation is `POST /v3/groups/:groupId/actions` (base URL `https://api.assetpanda.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-group-action.md) for the provider-specific parameters and requirements.

