# TMetric: Update Current User



```
PUT https://connect.mindcloud.co/v1/universal/tMetric/latest/actions/update-current-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TMetric `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/tMetric/latest/actions/update-current-user" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/tMetric/latest/actions/update-current-user', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `activeAccountId` | number | no | Workspace to make active for the current user. |
| `name` | string | no | Updated user name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accounts": [
        {
          "activity": {
            "blurScreenshots": true,
            "captureActivityLevels": true,
            "captureActivityLine": true,
            "captureAppsAndSites": true,
            "captureDetails": true,
            "captureScreenshots": true,
            "inactivityStopMinutes": 1
          },
          "firstWeekDay": 1,
          "id": 1,
          "name": "Ava Chen",
          "role": "string",
          "timeTracking": {
            "allowManualEditing": true,
            "allowNewClient": true,
            "allowNewProject": true,
            "allowNewTags": true,
            "allowNewTask": true,
            "allowTeamView": true,
            "requireDescription": true,
            "requireProject": true,
            "requireTags": true,
            "requireTask": true
          }
        }
      ],
      "activeAccountId": 1,
      "cultureInfo": {
        "id": "string",
        "nativeName": "Ava Chen"
      },
      "dateFormat": "string",
      "email": "ava@example.com",
      "iconUrl": "https://example.com",
      "id": 1,
      "name": "Ava Chen",
      "timeFormat": "string",
      "timeZone": {
        "currentOffset": 1,
        "displayName": "Ava Chen",
        "id": "string",
        "summerOffset": 1,
        "winterOffset": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accounts[].activity.blurScreenshots` | boolean |  |
| `accounts[].activity.captureActivityLevels` | boolean |  |
| `accounts[].activity.captureActivityLine` | boolean |  |
| `accounts[].activity.captureAppsAndSites` | boolean |  |
| `accounts[].activity.captureDetails` | boolean |  |
| `accounts[].activity.captureScreenshots` | boolean |  |
| `accounts[].activity.inactivityStopMinutes` | number |  |
| `accounts[].firstWeekDay` | number |  |
| `accounts[].id` | number |  |
| `accounts[].name` | string |  |
| `accounts[].role` | string |  |
| `accounts[].timeTracking.allowManualEditing` | boolean |  |
| `accounts[].timeTracking.allowNewClient` | boolean |  |
| `accounts[].timeTracking.allowNewProject` | boolean |  |
| `accounts[].timeTracking.allowNewTags` | boolean |  |
| `accounts[].timeTracking.allowNewTask` | boolean |  |
| `accounts[].timeTracking.allowTeamView` | boolean |  |
| `accounts[].timeTracking.requireDescription` | boolean |  |
| `accounts[].timeTracking.requireProject` | boolean |  |
| `accounts[].timeTracking.requireTags` | boolean |  |
| `accounts[].timeTracking.requireTask` | boolean |  |
| `activeAccountId` | number |  |
| `cultureInfo.id` | string |  |
| `cultureInfo.nativeName` | string |  |
| `dateFormat` | string |  |
| `email` | string |  |
| `iconUrl` | string |  |
| `id` | number |  |
| `name` | string |  |
| `timeFormat` | string |  |
| `timeZone.currentOffset` | number |  |
| `timeZone.displayName` | string |  |
| `timeZone.id` | string |  |
| `timeZone.summerOffset` | number |  |
| `timeZone.winterOffset` | number |  |

## Native endpoint

Through the native TMetric API, this operation is `PATCH /user` (base URL `https://app.tmetric.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-current-user.md) for the provider-specific parameters and requirements.

