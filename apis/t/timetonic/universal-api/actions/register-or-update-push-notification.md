# Timetonic: Register Or Update Push Notification

Creates or updates a push registration in Timetonic.

```
PUT https://connect.mindcloud.co/v1/universal/timetonic/latest/actions/register-or-update-push-notification
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Timetonic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/timetonic/latest/actions/register-or-update-push-notification" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "deviceId": "codex-test-device",
  "deviceType": "gcm_rid",
  "active": "FALSE",
  "registrationId": "codex-test-registration",
  "projectId": "codex-test-project"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/timetonic/latest/actions/register-or-update-push-notification', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "deviceId": "codex-test-device",
    "deviceType": "gcm_rid",
    "active": "FALSE",
    "registrationId": "codex-test-registration",
    "projectId": "codex-test-project"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `deviceId` | string | yes | Device identifier to register or update. Example: `codex-test-device`. |
| `deviceType` | string | yes | Push device type. Docs list gcm_rid, gcm_nk, ios_dt, ios_dt_v2, bb_dt, or win_uri. Example: `gcm_rid`. |
| `active` | string | yes | Whether the push registration is active. Example: `FALSE`. |
| `registrationId` | string | yes | Push registration token. Example: `codex-test-registration`. |
| `projectId` | string | yes | Push project identifier. Example: `codex-test-project`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdVNB": "string",
      "deviceID": 1,
      "req": "string",
      "sstamp": 1,
      "status": "string",
      "transactionId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdVNB` | string |  |
| `deviceID` | number |  |
| `req` | string |  |
| `sstamp` | number |  |
| `status` | string |  |
| `transactionId` | string |  |

## Native endpoint

Through the native Timetonic API, this operation is `POST` (base URL `https://timetonic.com/live/api.php`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/register-or-update-push-notification.md) for the provider-specific parameters and requirements.

