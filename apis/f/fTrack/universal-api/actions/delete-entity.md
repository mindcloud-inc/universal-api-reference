# FTrack: Delete Entity

Deletes an entity from FTrack.

```
DELETE https://connect.mindcloud.co/v1/universal/fTrack/latest/actions/delete-entity
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FTrack `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/fTrack/latest/actions/delete-entity?connectionId=$CONNECTION_ID&entityType=Task&entityKey=3f6d5b1e-8b49-4e8d-9ad3-d1f7a1234567" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "entityType": "Task",
  "entityKey": "3f6d5b1e-8b49-4e8d-9ad3-d1f7a1234567"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fTrack/latest/actions/delete-entity?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `entityType` | string | yes | Entity type to delete. Example: `Task`. |
| `entityKey` | string | yes | Key or id identifying the entity to delete. Example: `3f6d5b1e-8b49-4e8d-9ad3-d1f7a1234567`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native FTrack API returns.

## Native endpoint

Through the native FTrack API, this operation is `POST /api` (base URL `{{credentials.serverUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-entity.md) for the provider-specific parameters and requirements.

