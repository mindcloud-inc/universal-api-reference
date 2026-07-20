# Zenkit Universal API Examples

These examples use the MindCloud API key and Zenkit connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Current User

Retrieves the current user from Zenkit.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zenkit/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zenkit/latest/actions/get-current-user?${params}`, {
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
      "abTests": "string",
      "api_key": "string",
      "appInstances": [
        {
          "appType": "string",
          "created_at": "2026-05-07T12:00:00.000Z",
          "uuid": "string"
        }
      ],
      "backgroundId": "string",
      "blocked_at": "string",
      "blocked_by_organization_at": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "displayname": "Ava Chen",
      "emails": [
        {
          "created_at": "2026-05-07T12:00:00.000Z",
          "deprecated_at": "ava@example.com",
          "email": "ava@example.com",
          "id": 1,
          "isPrimary": true,
          "isVerified": true,
          "shortId": "ava@example.com",
          "updated_at": "2026-05-07T12:00:00.000Z",
          "uuid": "ava@example.com"
        }
      ],
      "fullname": "Ava Chen",
      "id": 1,
      "imageLink": "https://example.com",
      "initials": "string",
      "isImagePreferred": true,
      "isPasswordGenerated": true,
      "isSuperAdmin": true,
      "last_login": "2026-05-07T12:00:00.000Z",
      "last_organization_frozen_at": "string",
      "last_seen": "2026-05-07T12:00:00.000Z",
      "organizationId": 1,
      "privacy_policy_accepted_at": "2026-05-07T12:00:00.000Z",
      "providers": [
        {
          "created_at": "2026-05-07T12:00:00.000Z",
          "provider": "string",
          "uuid": "string"
        }
      ],
      "registered_at": "2026-05-07T12:00:00.000Z",
      "settings": {
        "assignmentsViewSettings": "string",
        "dateFormat": "string",
        "decimalFormat": 1,
        "defaultSortOrderForNewEntries": "string",
        "language": "string",
        "listActivityFilter": 1,
        "listElementSettingsInfoDismissed": true,
        "listEntryActivityFilter": 1,
        "notificationSettings": {
          "activities": {
            "desktopNotification": true,
            "email": true,
            "notification": true,
            "pushNotification": true,
            "toast": true
          },
          "comments": {
            "desktopNotification": true,
            "email": true,
            "notification": true,
            "pushNotification": true,
            "toast": true
          },
          "general": {
            "desktopNotification": true,
            "email": true,
            "notification": true,
            "pushNotification": true,
            "toast": true
          },
          "mentions": {
            "desktopNotification": true,
            "email": true,
            "notification": true,
            "pushNotification": true,
            "toast": true
          },
          "reactions": {
            "desktopNotification": true,
            "email": true,
            "notification": true,
            "pushNotification": true,
            "toast": true
          },
          "reminders": {
            "desktopNotification": true,
            "email": true,
            "notification": true,
            "pushNotification": true,
            "toast": true
          }
        },
        "recentListShortIds": [
          "string"
        ],
        "recentListsSettings": {
          "homeScreen": true,
          "navigationBarListsMenu": true
        },
        "soundEnabled": true,
        "startOfTheWeek": "string",
        "textfieldInfoDismissed": true,
        "themeOnboardingDismissed": true,
        "timeFormat": "string",
        "useDockedChats": true,
        "userActivityFilter": 1,
        "userAssignmentsInfoDismissed": true,
        "userCalendarSettings": "string",
        "userTagsInfoDismissed": true,
        "userTagsSettings": "string",
        "workspaceActivityFilter": 1
      },
      "shortId": "string",
      "terms_accepted_at": "2026-05-07T12:00:00.000Z",
      "timezone": "string",
      "username": "Ava Chen",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Current User action reference](actions/get-current-user.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/zenkit/latest/actions/get-current-user).

## Add Element To List

Creates a custom field in a Zenkit list.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zenkit/latest/actions/add-element-to-list" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "listId": "string",
  "items": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zenkit/latest/actions/add-element-to-list', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "listId": "string",
    "items": {}
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
      "created_at": "2026-05-07T12:00:00.000Z",
      "deprecated_at": "string",
      "description": "string",
      "displayName": "Ava Chen",
      "elementcategory": 1,
      "id": 1,
      "isAutoCreated": true,
      "isPrimary": true,
      "listId": 1,
      "name": "Ava Chen",
      "resourceRole": "string",
      "shortId": "string",
      "sortOrder": 1,
      "updated_at": "2026-05-07T12:00:00.000Z",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

See the full [Add Element To List action reference](actions/add-element-to-list.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/zenkit/latest/actions/add-element-to-list).
