# Strategypoint: List Notifications

Retrieves notifications from Strategypoint.

```
GET https://connect.mindcloud.co/v1/universal/strategypoint/latest/actions/list-notifications
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Strategypoint `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/strategypoint/latest/actions/list-notifications?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/strategypoint/latest/actions/list-notifications?${params}`, {
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
| `count` | number | no | Maximum number of notifications to return. |
| `object` | string | no | Filter notifications by related object type. |
| `objectId` | number | no | Filter notifications by related object identifier. |
| `periodId` | number | no | Filter notifications by period identifier. |
| `userId` | string | no | Filter notifications by user identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "elements": [
        {}
      ],
      "name": "Ava Chen",
      "notification": {},
      "notificationId": 1,
      "object": "string",
      "periodOffset": 1,
      "sortOrder": 1,
      "userId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `elements` | array<object> | The related elements returned with the notification. |
| `name` | string | The notification name. |
| `notification` | object | The embedded notification definition. |
| `notificationId` | number | The unique notification identifier. |
| `object` | string | The related object type. |
| `periodOffset` | number | The configured period offset. |
| `sortOrder` | number | The sort order for the notification. |
| `userId` | number | The related user identifier. |

## Native endpoint

Through the native Strategypoint API, this operation is `GET /notifications` (base URL `https://app.clearpointstrategy.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-notifications.md) for the provider-specific parameters and requirements.

