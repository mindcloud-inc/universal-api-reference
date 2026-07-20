# Timeular: Unarchive Activity

Unarchives an existing activity in your Timeular workspace.

```
PUT https://connect.mindcloud.co/v1/universal/timeular/latest/actions/unarchive-activity
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Timeular `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/timeular/latest/actions/unarchive-activity" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "activityId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/timeular/latest/actions/unarchive-activity', {
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

## Response

```json
{
  "success": true,
  "data": [
    {
      "color": "string",
      "folderId": "string",
      "id": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `color` | string |  |
| `folderId` | string |  |
| `id` | string |  |
| `name` | string |  |

## Native endpoint

Through the native Timeular API, this operation is `POST /api/v4/activities/:activityId/unarchive` (base URL `https://api.early.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/unarchive-activity.md) for the provider-specific parameters and requirements.

