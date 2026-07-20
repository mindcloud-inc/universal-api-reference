# Clockify Universal API Examples

These examples use the MindCloud API key and Clockify connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Current User

Retrieves the current user from Clockify.

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

Example response:

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

See the full [Get Current User action reference](actions/get-current-user.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/clockify/latest/actions/get-current-user).

## Add Manager Role to User

Adds the manager role to a user in Clockify.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/clockify/latest/actions/add-manager-role-to-user" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "workspaceId": "string",
  "userId": "string",
  "entityId": "string",
  "role": "PROJECT_MANAGER"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/clockify/latest/actions/add-manager-role-to-user', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "workspaceId": "string",
    "userId": "string",
    "entityId": "string",
    "role": "PROJECT_MANAGER"
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "role": {
        "id": "string",
        "name": "Ava Chen",
        "source": {
          "id": "string",
          "type": "string"
        }
      },
      "userId": "string",
      "workspaceId": "string"
    }
  ],
  "meta": {}
}
```

See the full [Add Manager Role to User action reference](actions/add-manager-role-to-user.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/clockify/latest/actions/add-manager-role-to-user).
