# Invidious: Remove Auth Subscription



```
DELETE https://connect.mindcloud.co/v1/universal/invidious/latest/actions/remove-auth-subscription
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Invidious `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/invidious/latest/actions/remove-auth-subscription?connectionId=$CONNECTION_ID&channelId=UC_x5XG1OV2P6uZZ5FSM9Ttw" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "channelId": "UC_x5XG1OV2P6uZZ5FSM9Ttw"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/invidious/latest/actions/remove-auth-subscription?${params}`, {
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
| `channelId` | string | yes | Channel UCID to unsubscribe from. Example: `UC_x5XG1OV2P6uZZ5FSM9Ttw`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "authorId": "string",
      "message": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `authorId` | string |  |
| `message` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native Invidious API, this operation is `DELETE /auth/subscriptions/:ucid` (base URL `{{credentials.instanceUrl}}/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-auth-subscription.md) for the provider-specific parameters and requirements.

