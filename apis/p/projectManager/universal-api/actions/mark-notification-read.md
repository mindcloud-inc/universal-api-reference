# ProjectManager: Mark Notification Read

Marks a notification as read in ProjectManager.

```
POST https://connect.mindcloud.co/v1/universal/projectManager/latest/actions/mark-notification-read
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ProjectManager `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/projectManager/latest/actions/mark-notification-read" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "77777777-7777-7777-7777-777777777777"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/projectManager/latest/actions/mark-notification-read', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "77777777-7777-7777-7777-777777777777"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | The unique identifier of the notification to mark read Example: `77777777-7777-7777-7777-777777777777`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "timestamp": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `timestamp` | string |  |

## Native endpoint

Through the native ProjectManager API, this operation is `POST /api/data/notifications/:id/markread` (base URL `https://api.projectmanager.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/mark-notification-read.md) for the provider-specific parameters and requirements.

