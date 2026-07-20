# Vybit: Trigger Vybit Notification



```
POST https://connect.mindcloud.co/v1/universal/vybit/latest/actions/trigger-vybit-notification
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vybit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/vybit/latest/actions/trigger-vybit-notification" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "key": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/vybit/latest/actions/trigger-vybit-notification', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "key": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `imageUrl` | string | no | Custom image URL |
| `key` | string | yes | The unique key of the vybit to trigger. |
| `linkUrl` | string | no | Custom link URL |
| `log` | string | no | Log entry to append to the vybit log |
| `message` | string | no | Custom notification message |
| `runOnce` | boolean | no | Disable the vybit after this trigger fires |

## Response

```json
{
  "success": true,
  "data": [
    {
      "plk": "string",
      "result": 1,
      "warn": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `plk` | string |  |
| `result` | number |  |
| `warn` | string |  |

## Native endpoint

Through the native Vybit API, this operation is `POST /vybit/{{key}}/trigger` (base URL `https://api.vybit.net/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/trigger-vybit-notification.md) for the provider-specific parameters and requirements.

