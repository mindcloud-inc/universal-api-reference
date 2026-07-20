# Fibery: Create Or Update Entities

Creates or updates entities in Fibery.

```
PUT https://connect.mindcloud.co/v1/universal/fibery/latest/actions/create-or-update-entities
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fibery `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/fibery/latest/actions/create-or-update-entities" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "type": "string",
  "entities[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/fibery/latest/actions/create-or-update-entities', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "type": "string",
    "entities[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `type` | string | yes | Fibery type name shared by all entities in the batch. |
| `entities[]` | array<object> | yes | Array of entities to create or update. |
| `conflictField` | string | no | Field used to match existing entities when an item has no Fibery ID. |
| `conflictAction` | string | no | What Fibery should do on conflict, for example `merge` or `skip`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Fibery API returns.

## Native endpoint

Through the native Fibery API, this operation is `POST /commands` (base URL `https://{{credentials.account}}.fibery.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-or-update-entities.md) for the provider-specific parameters and requirements.

