# Sleekplan: Get Unread Notification Count



```
GET https://connect.mindcloud.co/v1/universal/sleekplan/latest/actions/get-unread-notification-count
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sleekplan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sleekplan/latest/actions/get-unread-notification-count?connectionId=$CONNECTION_ID&userId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "userId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sleekplan/latest/actions/get-unread-notification-count?${params}`, {
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
| `userId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "notifications": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `notifications` | number |  |

## Native endpoint

Through the native Sleekplan API, this operation is `GET /user/:userid/notifications/count` (base URL `https://api.sleekplan.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-unread-notification-count.md) for the provider-specific parameters and requirements.

