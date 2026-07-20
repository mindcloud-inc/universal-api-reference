# Unstructured: Get Notification

Retrieves a notification from Unstructured.

```
GET https://connect.mindcloud.co/v1/universal/unstructured/latest/actions/get-notification
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Unstructured `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/unstructured/latest/actions/get-notification?connectionId=$CONNECTION_ID&notificationId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "notificationId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/unstructured/latest/actions/get-notification?${params}`, {
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
| `notificationId` | string | yes | Notification ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "channelId": "string",
      "createdAt": "string",
      "eventType": "string",
      "id": "string",
      "jobId": "string",
      "payload": {},
      "readAt": "string",
      "workflowId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `channelId` | string | Notification channel ID. |
| `createdAt` | string | Creation timestamp. |
| `eventType` | string | Notification event type. |
| `id` | string | Notification ID. |
| `jobId` | string | Job ID related to the notification. |
| `payload` | object | Notification payload. |
| `readAt` | string | Read timestamp. |
| `workflowId` | string | Workflow ID related to the notification. |

## Native endpoint

Through the native Unstructured API, this operation is `GET /notifications/:notification_id` (base URL `https://platform.unstructuredapp.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-notification.md) for the provider-specific parameters and requirements.

