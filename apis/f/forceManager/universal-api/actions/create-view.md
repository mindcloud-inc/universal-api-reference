# ForceManager: Create View

Creates a new view in ForceManager.

```
POST https://connect.mindcloud.co/v1/universal/forceManager/latest/actions/create-view
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ForceManager `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/forceManager/latest/actions/create-view" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "entity": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/forceManager/latest/actions/create-view', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "entity": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Name of the view. |
| `entity` | string | yes | Entity where the view filter was applied. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "enddate": "2026-05-07T12:00:00.000Z",
      "entity": "string",
      "id": 1,
      "isActive": true,
      "isPublic": true,
      "name": "Ava Chen",
      "startdate": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `enddate` | date | Date until when the view filter will be visible. |
| `entity` | string | Entity where the view filter was applied. |
| `id` | number | Unique identifier for the view. |
| `isActive` | boolean | Whether the view is active. |
| `isPublic` | boolean | Whether the view is visible to all users. |
| `name` | string | Name of the view. |
| `startdate` | date | Date the view filter was made visible. |

## Native endpoint

Through the native ForceManager API, this operation is `POST /views`. The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-view.md) for the provider-specific parameters and requirements.

