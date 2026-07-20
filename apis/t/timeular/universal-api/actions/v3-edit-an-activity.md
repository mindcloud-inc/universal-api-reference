# Timeular: V3 Edit an Activity

Updates an existing activity in the Timeular v3 API.

```
PUT https://connect.mindcloud.co/v1/universal/timeular/latest/actions/v3-edit-an-activity
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Timeular `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/timeular/latest/actions/v3-edit-an-activity" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "activityId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/timeular/latest/actions/v3-edit-an-activity', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "activityId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `activityId` | string | yes |  |
| `color` | string | no |  |
| `name` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "color": "string",
      "id": "string",
      "integration": "string",
      "name": "Ava Chen",
      "spaceId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `color` | string |  |
| `id` | string |  |
| `integration` | string |  |
| `name` | string |  |
| `spaceId` | string |  |

## Native endpoint

Through the native Timeular API, this operation is `PATCH /api/v3/activities/:activityId` (base URL `https://api.early.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/v3-edit-an-activity.md) for the provider-specific parameters and requirements.

