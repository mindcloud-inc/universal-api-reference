# FTrack: Convert Entity Type

Converts an entity type in FTrack.

```
PUT https://connect.mindcloud.co/v1/universal/fTrack/latest/actions/convert-entity-type
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FTrack `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/fTrack/latest/actions/convert-entity-type" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "entityType": "Task",
  "entityKey": "3f6d5b1e-8b49-4e8d-9ad3-d1f7a1234567",
  "targetEntityType": "Shot"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/fTrack/latest/actions/convert-entity-type', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "entityType": "Task",
    "entityKey": "3f6d5b1e-8b49-4e8d-9ad3-d1f7a1234567",
    "targetEntityType": "Shot"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `entityType` | string | yes | Current entity type. Example: `Task`. |
| `entityKey` | string | yes | Key or id identifying the entity to convert. Example: `3f6d5b1e-8b49-4e8d-9ad3-d1f7a1234567`. |
| `targetEntityType` | string | yes | Entity type to convert the record into. Example: `Shot`. |
| `entityData` | object | no | Optional attributes to apply during conversion. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native FTrack API returns.

## Native endpoint

Through the native FTrack API, this operation is `POST /api` (base URL `{{credentials.serverUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/convert-entity-type.md) for the provider-specific parameters and requirements.

