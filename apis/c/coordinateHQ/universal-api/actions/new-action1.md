# CoordinateHQ: Attach Task File



```
POST https://connect.mindcloud.co/v1/universal/coordinateHQ/latest/actions/new-action1
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CoordinateHQ `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/coordinateHQ/latest/actions/new-action1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "File": "string",
  "task_id": "string",
  "project_id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/coordinateHQ/latest/actions/new-action1', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "File": "string",
    "task_id": "string",
    "project_id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `File` | file | yes |  |
| `task_id` | string | yes |  |
| `project_id` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "response": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `response` | string |  |

## Native endpoint

Through the native CoordinateHQ API, this operation is `POST /projects/:project_id/task/:task_id/files/attach` (base URL `https://app.coordinatehq.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/new-action1.md) for the provider-specific parameters and requirements.

