# XenForo: Send Alert

Sends an alert to a user in XenForo.

```
POST https://connect.mindcloud.co/v1/universal/xenForo/latest/actions/send-alert
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a XenForo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/xenForo/latest/actions/send-alert" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "toUserId": "1",
  "alert": "You have a new update: {link}"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/xenForo/latest/actions/send-alert', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "toUserId": "1",
    "alert": "You have a new update: {link}"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `toUserId` | number | yes | ID of the user who will receive the alert. Example: `1`. |
| `alert` | string | yes | Alert text. Use {link} where the link should be inserted. Example: `You have a new update: {link}`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fromUserId` | number | no | Optional user ID to send the alert from. Use 0 for an anonymous alert. Example: `0`. |
| `linkUrl` | string | no | Optional URL opened when the alert is clicked. Example: `https://community.example.com/threads/example.1/`. |
| `linkTitle` | string | no | Optional link text shown with the alert. Example: `View update`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean | Whether the alert was sent. |

## Native endpoint

Through the native XenForo API, this operation is `POST /alerts/` (base URL `{{credentials.baseUrl}}/2310/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-alert.md) for the provider-specific parameters and requirements.

