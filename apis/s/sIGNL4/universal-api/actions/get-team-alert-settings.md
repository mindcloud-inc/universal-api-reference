# SIGNL4: Get Team Alert Settings

Retrieves alert settings for a team from SIGNL4.

```
GET https://connect.mindcloud.co/v1/universal/sIGNL4/latest/actions/get-team-alert-settings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SIGNL4 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sIGNL4/latest/actions/get-team-alert-settings?connectionId=$CONNECTION_ID&teamId=sample-team-id" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "teamId": "sample-team-id"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sIGNL4/latest/actions/get-team-alert-settings?${params}`, {
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
| `teamId` | string | yes | SIGNL4 team ID. Example: `sample-team-id`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "escEnabled": true,
      "escMode": 1,
      "filterAction": 1,
      "filterMode": 1,
      "notificationProfileOverrides": {
        "channel": 1,
        "delay": 1,
        "enabled": true
      },
      "notifyOnAlertStatus": 1,
      "optOut": 1,
      "overrideNotificationProfiles": true,
      "persNotInterval": 1,
      "persNotMode": 1,
      "responseMode": 1,
      "responseTime": 1,
      "signalingMode": 1,
      "tierResponseTime": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `escEnabled` | boolean |  |
| `escMode` | number |  |
| `filterAction` | number |  |
| `filterMode` | number |  |
| `notificationProfileOverrides` | array<object> |  |
| `notificationProfileOverrides.channel` | number |  |
| `notificationProfileOverrides.delay` | number |  |
| `notificationProfileOverrides.enabled` | boolean |  |
| `notifyOnAlertStatus` | number |  |
| `optOut` | number |  |
| `overrideNotificationProfiles` | boolean |  |
| `persNotInterval` | number |  |
| `persNotMode` | number |  |
| `responseMode` | number |  |
| `responseTime` | number |  |
| `signalingMode` | number |  |
| `tierResponseTime` | number |  |

## Native endpoint

Through the native SIGNL4 API, this operation is `GET /v2/teams/{teamId}/alertSettings` (base URL `https://connect.signl4.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-team-alert-settings.md) for the provider-specific parameters and requirements.

