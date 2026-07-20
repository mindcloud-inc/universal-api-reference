# OneSignal: Get User

Retrieves a user from OneSignal by alias.

```
GET https://connect.mindcloud.co/v1/universal/oneSignal/latest/actions/get-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OneSignal `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oneSignal/latest/actions/get-user?connectionId=$CONNECTION_ID&aliasId=string&aliasLabel=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "aliasId": "string",
  "aliasLabel": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oneSignal/latest/actions/get-user?${params}`, {
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
| `aliasId` | string | yes | The alias value for the user to fetch. |
| `aliasLabel` | string | yes | The alias type to look up, such as external_id. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "identity": {
        "externalId": "string",
        "onesignalId": "string"
      },
      "properties": {
        "firstActive": "2026-05-07T12:00:00.000Z",
        "lastActive": "2026-05-07T12:00:00.000Z"
      },
      "subscriptions": [
        {
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
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `identity.externalId` | string |  |
| `identity.onesignalId` | string |  |
| `properties.firstActive` | date |  |
| `properties.lastActive` | date |  |
| `subscriptions[].appId` | string |  |
| `subscriptions[].appVersion` | string |  |
| `subscriptions[].carrier` | string |  |
| `subscriptions[].deviceModel` | string |  |
| `subscriptions[].deviceOs` | string |  |
| `subscriptions[].enabled` | boolean |  |
| `subscriptions[].id` | string |  |
| `subscriptions[].netType` | number |  |
| `subscriptions[].notificationTypes` | number |  |
| `subscriptions[].rooted` | boolean |  |
| `subscriptions[].sdk` | string |  |
| `subscriptions[].sessionCount` | number |  |
| `subscriptions[].sessionTime` | number |  |
| `subscriptions[].testType` | number |  |
| `subscriptions[].token` | string |  |
| `subscriptions[].type` | string |  |
| `subscriptions[].webAuth` | string |  |
| `subscriptions[].webP256` | string |  |

## Native endpoint

Through the native OneSignal API, this operation is `GET /apps/:app_id/users/by/:alias_label/:alias_id` (base URL `https://api.onesignal.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user.md) for the provider-specific parameters and requirements.

