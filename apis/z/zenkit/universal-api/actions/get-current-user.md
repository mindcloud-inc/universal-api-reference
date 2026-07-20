# Zenkit: Get Current User

Retrieves the current user from Zenkit.

```
GET https://connect.mindcloud.co/v1/universal/zenkit/latest/actions/get-current-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zenkit `connectionId` ([setup](../authentication.md)).

## Example request

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



## Response

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

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `abTests` | string |  |
| `api_key` | string |  |
| `appInstances[].appType` | string |  |
| `appInstances[].created_at` | date |  |
| `appInstances[].uuid` | string |  |
| `backgroundId` | string |  |
| `blocked_at` | string |  |
| `blocked_by_organization_at` | string |  |
| `created_at` | date |  |
| `displayname` | string |  |
| `emails[].created_at` | date |  |
| `emails[].deprecated_at` | string |  |
| `emails[].email` | string |  |
| `emails[].id` | number |  |
| `emails[].isPrimary` | boolean |  |
| `emails[].isVerified` | boolean |  |
| `emails[].shortId` | string |  |
| `emails[].updated_at` | date |  |
| `emails[].uuid` | string |  |
| `fullname` | string |  |
| `id` | number |  |
| `imageLink` | string |  |
| `initials` | string |  |
| `isImagePreferred` | boolean |  |
| `isPasswordGenerated` | boolean |  |
| `isSuperAdmin` | boolean |  |
| `last_login` | date |  |
| `last_organization_frozen_at` | string |  |
| `last_seen` | date |  |
| `organizationId` | number |  |
| `privacy_policy_accepted_at` | date |  |
| `providers[].created_at` | date |  |
| `providers[].provider` | string |  |
| `providers[].uuid` | string |  |
| `registered_at` | date |  |
| `settings.assignmentsViewSettings` | string |  |
| `settings.dateFormat` | string |  |
| `settings.decimalFormat` | number |  |
| `settings.defaultSortOrderForNewEntries` | string |  |
| `settings.language` | string |  |
| `settings.listActivityFilter` | number |  |
| `settings.listElementSettingsInfoDismissed` | boolean |  |
| `settings.listEntryActivityFilter` | number |  |
| `settings.notificationSettings.activities.desktopNotification` | boolean |  |
| `settings.notificationSettings.activities.email` | boolean |  |
| `settings.notificationSettings.activities.notification` | boolean |  |
| `settings.notificationSettings.activities.pushNotification` | boolean |  |
| `settings.notificationSettings.activities.toast` | boolean |  |
| `settings.notificationSettings.comments.desktopNotification` | boolean |  |
| `settings.notificationSettings.comments.email` | boolean |  |
| `settings.notificationSettings.comments.notification` | boolean |  |
| `settings.notificationSettings.comments.pushNotification` | boolean |  |
| `settings.notificationSettings.comments.toast` | boolean |  |
| `settings.notificationSettings.general.desktopNotification` | boolean |  |
| `settings.notificationSettings.general.email` | boolean |  |
| `settings.notificationSettings.general.notification` | boolean |  |
| `settings.notificationSettings.general.pushNotification` | boolean |  |
| `settings.notificationSettings.general.toast` | boolean |  |
| `settings.notificationSettings.mentions.desktopNotification` | boolean |  |
| `settings.notificationSettings.mentions.email` | boolean |  |
| `settings.notificationSettings.mentions.notification` | boolean |  |
| `settings.notificationSettings.mentions.pushNotification` | boolean |  |
| `settings.notificationSettings.mentions.toast` | boolean |  |
| `settings.notificationSettings.reactions.desktopNotification` | boolean |  |
| `settings.notificationSettings.reactions.email` | boolean |  |
| `settings.notificationSettings.reactions.notification` | boolean |  |
| `settings.notificationSettings.reactions.pushNotification` | boolean |  |
| `settings.notificationSettings.reactions.toast` | boolean |  |
| `settings.notificationSettings.reminders.desktopNotification` | boolean |  |
| `settings.notificationSettings.reminders.email` | boolean |  |
| `settings.notificationSettings.reminders.notification` | boolean |  |
| `settings.notificationSettings.reminders.pushNotification` | boolean |  |
| `settings.notificationSettings.reminders.toast` | boolean |  |
| `settings.recentListShortIds[]` | string |  |
| `settings.recentListsSettings.homeScreen` | boolean |  |
| `settings.recentListsSettings.navigationBarListsMenu` | boolean |  |
| `settings.soundEnabled` | boolean |  |
| `settings.startOfTheWeek` | string |  |
| `settings.textfieldInfoDismissed` | boolean |  |
| `settings.themeOnboardingDismissed` | boolean |  |
| `settings.timeFormat` | string |  |
| `settings.useDockedChats` | boolean |  |
| `settings.userActivityFilter` | number |  |
| `settings.userAssignmentsInfoDismissed` | boolean |  |
| `settings.userCalendarSettings` | string |  |
| `settings.userTagsInfoDismissed` | boolean |  |
| `settings.userTagsSettings` | string |  |
| `settings.workspaceActivityFilter` | number |  |
| `shortId` | string |  |
| `terms_accepted_at` | date |  |
| `timezone` | string |  |
| `username` | string |  |
| `uuid` | string |  |

## Native endpoint

Through the native Zenkit API, this operation is `GET /users/me` (base URL `https://zenkit.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-current-user.md) for the provider-specific parameters and requirements.

