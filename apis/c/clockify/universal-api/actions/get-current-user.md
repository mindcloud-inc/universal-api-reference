# Clockify: Get Current User

Retrieves the current user from Clockify.

```
GET https://connect.mindcloud.co/v1/universal/clockify/latest/actions/get-current-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clockify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clockify/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clockify/latest/actions/get-current-user?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "activeWorkspace": "string",
      "defaultWorkspace": "string",
      "email": "ava@example.com",
      "id": "string",
      "name": "Ava Chen",
      "profilePicture": "string",
      "settings": {
        "alerts": true,
        "approval": true,
        "collapseAllProjectLists": true,
        "dashboardPinToTop": true,
        "dashboardSelection": "string",
        "dashboardViewType": "string",
        "dateFormat": "string",
        "groupSimilarEntriesDisabled": true,
        "invoiceReminders": true,
        "isCompactViewOn": true,
        "lang": "string",
        "longRunning": true,
        "multiFactorEnabled": true,
        "myStartOfDay": "string",
        "onboarding": true,
        "projectListCollapse": 1,
        "projectPickerTaskFilter": true,
        "pto": true,
        "reminders": true,
        "scheduledReports": true,
        "scheduling": true,
        "sendNewsletter": true,
        "showOnlyWorkingDays": true,
        "summaryReportSettings": {
          "group": "string",
          "subgroup": "string"
        },
        "theme": "string",
        "timeFormat": "string",
        "timeTrackingManual": true,
        "timeZone": "string",
        "weeklyUpdates": true,
        "weekStart": "string"
      },
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `activeWorkspace` | string |  |
| `defaultWorkspace` | string |  |
| `email` | string |  |
| `id` | string |  |
| `name` | string |  |
| `profilePicture` | string |  |
| `settings.alerts` | boolean |  |
| `settings.approval` | boolean |  |
| `settings.collapseAllProjectLists` | boolean |  |
| `settings.dashboardPinToTop` | boolean |  |
| `settings.dashboardSelection` | string |  |
| `settings.dashboardViewType` | string |  |
| `settings.dateFormat` | string |  |
| `settings.groupSimilarEntriesDisabled` | boolean |  |
| `settings.invoiceReminders` | boolean |  |
| `settings.isCompactViewOn` | boolean |  |
| `settings.lang` | string |  |
| `settings.longRunning` | boolean |  |
| `settings.multiFactorEnabled` | boolean |  |
| `settings.myStartOfDay` | string |  |
| `settings.onboarding` | boolean |  |
| `settings.projectListCollapse` | number |  |
| `settings.projectPickerTaskFilter` | boolean |  |
| `settings.pto` | boolean |  |
| `settings.reminders` | boolean |  |
| `settings.scheduledReports` | boolean |  |
| `settings.scheduling` | boolean |  |
| `settings.sendNewsletter` | boolean |  |
| `settings.showOnlyWorkingDays` | boolean |  |
| `settings.summaryReportSettings.group` | string |  |
| `settings.summaryReportSettings.subgroup` | string |  |
| `settings.theme` | string |  |
| `settings.timeFormat` | string |  |
| `settings.timeTrackingManual` | boolean |  |
| `settings.timeZone` | string |  |
| `settings.weeklyUpdates` | boolean |  |
| `settings.weekStart` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Clockify API, this operation is `GET user` (base URL `https://api.clockify.me/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-current-user.md) for the provider-specific parameters and requirements.

