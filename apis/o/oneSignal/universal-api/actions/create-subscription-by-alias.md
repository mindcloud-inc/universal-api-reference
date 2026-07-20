# OneSignal: Create Subscription by Alias

Creates a subscription in OneSignal by alias.

```
POST https://connect.mindcloud.co/v1/universal/oneSignal/latest/actions/create-subscription-by-alias
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OneSignal `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/oneSignal/latest/actions/create-subscription-by-alias" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "aliasId": "string",
  "aliasLabel": "string",
  "subscription": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/oneSignal/latest/actions/create-subscription-by-alias', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "aliasId": "string",
    "aliasLabel": "string",
    "subscription": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `aliasId` | string | yes | The alias value for the selected alias label. |
| `aliasLabel` | string | yes | The alias namespace to look up, such as external_id. |
| `subscription` | object | yes | The subscription object to create for the user. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "subscription": {
        "appId": "string",
        "appVersion": "string",
        "carrier": "string",
        "deviceModel": "string",
        "deviceOs": "string",
        "enabled": true,
        "id": "string",
        "netType": 1,
        "notificationTypes": 1,
        "rooted": true,
        "sdk": "string",
        "sessionCount": 1,
        "sessionTime": 1,
        "testType": 1,
        "token": "string",
        "type": "string",
        "webAuth": "string",
        "webP256": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `subscription.appId` | string |  |
| `subscription.appVersion` | string |  |
| `subscription.carrier` | string |  |
| `subscription.deviceModel` | string |  |
| `subscription.deviceOs` | string |  |
| `subscription.enabled` | boolean |  |
| `subscription.id` | string |  |
| `subscription.netType` | number |  |
| `subscription.notificationTypes` | number |  |
| `subscription.rooted` | boolean |  |
| `subscription.sdk` | string |  |
| `subscription.sessionCount` | number |  |
| `subscription.sessionTime` | number |  |
| `subscription.testType` | number |  |
| `subscription.token` | string |  |
| `subscription.type` | string |  |
| `subscription.webAuth` | string |  |
| `subscription.webP256` | string |  |

## Native endpoint

Through the native OneSignal API, this operation is `POST /apps/:app_id/users/by/:alias_label/:alias_id/subscriptions` (base URL `https://api.onesignal.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-subscription-by-alias.md) for the provider-specific parameters and requirements.

