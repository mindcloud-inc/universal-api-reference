# Unstructured: Mark Notifications As Read

Marks notifications as read in Unstructured.

```
PUT https://connect.mindcloud.co/v1/universal/unstructured/latest/actions/mark-notifications-as-read
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Unstructured `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/unstructured/latest/actions/mark-notifications-as-read" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/unstructured/latest/actions/mark-notifications-as-read', {
  method: 'PUT',
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
| `notificationIds[]` | array<string> | no | Notification IDs to mark as read. |
| `before` | string | no | Mark all notifications before this time as read. |
| `markAll` | boolean | no | Mark all notifications as read. |
| `workflowId` | string | no | Workflow filter when marking notifications as read. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "markedCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `markedCount` | number | Number of notifications marked as read. |

## Native endpoint

Through the native Unstructured API, this operation is `POST /notifications/mark-read` (base URL `https://platform.unstructuredapp.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/mark-notifications-as-read.md) for the provider-specific parameters and requirements.

