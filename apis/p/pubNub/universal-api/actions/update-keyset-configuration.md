# PubNub: Update Keyset Configuration

Updates keyset configuration in PubNub.

```
PUT https://connect.mindcloud.co/v1/universal/pubNub/latest/actions/update-keyset-configuration
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PubNub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/pubNub/latest/actions/update-keyset-configuration" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "presence.enabled": true
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pubNub/latest/actions/update-keyset-configuration', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "presence.enabled": true
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | The PubNub keyset ID. |
| `presence.enabled` | boolean | yes | Whether presence is enabled for the keyset. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accessManager": {},
      "apns": {},
      "appContext": {},
      "fcm": {},
      "files": {},
      "messagePersistence": {},
      "presence": {},
      "streamController": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accessManager` | object | Access Manager settings. |
| `apns` | object | APNS settings. |
| `appContext` | object | App Context settings. |
| `fcm` | object | FCM settings. |
| `files` | object | Files settings. |
| `messagePersistence` | object | Message persistence settings. |
| `presence` | object | Presence settings. |
| `streamController` | object | Stream Controller settings. |

## Native endpoint

Through the native PubNub API, this operation is `PATCH /keysets/:id/config` (base URL `https://admin-api.pubnub.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-keyset-configuration.md) for the provider-specific parameters and requirements.

