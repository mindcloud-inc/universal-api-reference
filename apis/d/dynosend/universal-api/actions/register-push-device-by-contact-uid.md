# Dynosend: Register Push Device by Contact UID

Registers a push device in Dynosend by contact UID.

```
POST https://connect.mindcloud.co/v1/universal/dynosend/latest/actions/register-push-device-by-contact-uid
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dynosend `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/dynosend/latest/actions/register-push-device-by-contact-uid" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "appId": "string",
  "contactUid": "string",
  "fcmToken": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dynosend/latest/actions/register-push-device-by-contact-uid', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "appId": "string",
    "contactUid": "string",
    "fcmToken": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `appId` | string | yes | The Dynosend mobile push project ID. |
| `contactUid` | string | yes | The UID of the Dynosend contact that owns the device. |
| `fcmToken` | string | yes | The Firebase Cloud Messaging device token to register. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Dynosend API returns.

## Native endpoint

Through the native Dynosend API, this operation is `POST https://api.dynosend.com/device/register` (base URL `https://api.dynosend.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/register-push-device-by-contact-uid.md) for the provider-specific parameters and requirements.

