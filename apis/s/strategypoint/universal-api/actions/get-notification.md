# Strategypoint: Get Notification

Retrieves a notification from Strategypoint.

```
GET https://connect.mindcloud.co/v1/universal/strategypoint/latest/actions/get-notification
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Strategypoint `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/strategypoint/latest/actions/get-notification?connectionId=$CONNECTION_ID&notificationId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "notificationId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/strategypoint/latest/actions/get-notification?${params}`, {
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
| `notificationId` | number | yes | The unique notification identifier. |
| `object` | string | no | Resolve the notification in the context of a related object type. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "action": "string",
      "criteria": "string",
      "detectionType": "string",
      "name": "Ava Chen",
      "notificationId": 1,
      "object": "string",
      "periodOffset": 1,
      "userId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `action` | string | The action performed by the notification. |
| `criteria` | string | The notification criteria. |
| `detectionType` | string | The detection type used by the notification. |
| `name` | string | The notification name. |
| `notificationId` | number | The unique notification identifier. |
| `object` | string | The related object type. |
| `periodOffset` | number | The configured period offset. |
| `userId` | number | The related user identifier. |

## Native endpoint

Through the native Strategypoint API, this operation is `GET /notifications/{notificationId}` (base URL `https://app.clearpointstrategy.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-notification.md) for the provider-specific parameters and requirements.

