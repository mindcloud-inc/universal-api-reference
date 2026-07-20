# Zulip: Get Subscription Status

Retrieves a user's subscription status for a Zulip channel.

```
GET https://connect.mindcloud.co/v1/universal/zulip/latest/actions/get-subscription-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zulip `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zulip/latest/actions/get-subscription-status?connectionId=$CONNECTION_ID&streamId=1&userId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "streamId": "1",
  "userId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zulip/latest/actions/get-subscription-status?${params}`, {
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
| `streamId` | number | yes | The target channel ID. |
| `userId` | number | yes | The target user's ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "is_subscribed": true,
      "msg": "string",
      "result": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `is_subscribed` | boolean |  |
| `msg` | string |  |
| `result` | string |  |

## Native endpoint

Through the native Zulip API, this operation is `GET /users/:user_id/subscriptions/:stream_id` (base URL `{{credentials.site}}/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-subscription-status.md) for the provider-specific parameters and requirements.

