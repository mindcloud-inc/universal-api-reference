# ForceManager: Update View

Updates an existing view in ForceManager.

```
PUT https://connect.mindcloud.co/v1/universal/forceManager/latest/actions/update-view
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ForceManager `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/forceManager/latest/actions/update-view" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/forceManager/latest/actions/update-view', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | Unique identifier for the view. |

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

Through the native ForceManager API, this operation is `PUT /views`. The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-view.md) for the provider-specific parameters and requirements.

