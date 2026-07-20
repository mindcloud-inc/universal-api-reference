# Vybit: Trigger Vybit Notification (Legacy OAuth)



```
POST https://connect.mindcloud.co/v1/universal/vybit/latest/actions/trigger-vybit-notification-legacy-oauth
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vybit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/vybit/latest/actions/trigger-vybit-notification-legacy-oauth" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "triggerKey": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/vybit/latest/actions/trigger-vybit-notification-legacy-oauth', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "triggerKey": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `imageUrl` | string | no | Optional image URL to attach to the notification. |
| `linkUrl` | string | no | Optional redirect URL when the notification is tapped. |
| `log` | string | no | Optional content to append to the Vybit log. |
| `message` | string | no | Optional message to display with the notification. |
| `triggerKey` | string | yes | The legacy trigger key of the vybit to fire. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "plk": "string",
      "result": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `plk` | string | Processing key returned for the triggered notification. |
| `result` | number | Result code from the legacy trigger endpoint. |

## Native endpoint

Through the native Vybit API, this operation is `POST /fire/{{triggerKey}}` (base URL `https://api.vybit.net/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/trigger-vybit-notification-legacy-oauth.md) for the provider-specific parameters and requirements.

