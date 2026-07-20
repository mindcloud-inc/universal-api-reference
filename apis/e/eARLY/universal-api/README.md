# <img src="https://images.mindcloud.co/apps/icons/screenshot-2026-03-25-154708_1774464749478.png" alt="EARLY logo" width="28" height="28"> EARLY: Universal API

Effortless time tracking app with leave management, a physical time tracker, and automatic tracking.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/eARLY/latest
- **Category:** Human Resources / HRIS
- **Actions:** 48
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://early.app
- **Vendor API docs:** https://developers.early.app/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Generate Report](actions/generate-report.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eARLY/latest/actions/generate-report?connectionId=$CONNECTION_ID&date.start=string&date.end=string&fileType=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (48)

### Activity

| Action | Method | Description |
| --- | --- | --- |
| [Archive Activity](actions/archive-activity.md) | DELETE | Archives an activity in EARLY. |
| [Create Activity](actions/create-activity.md) | POST | Creates a new activity in EARLY. |
| [List Activities](actions/list-activities.md) | GET | Retrieves activities from EARLY. |
| [Unarchive Activity](actions/unarchive-activity.md) | PUT | Unarchives an activity in EARLY. |
| [Update Activity](actions/update-activity.md) | PUT | Updates an activity in EARLY. |

### Folder

| Action | Method | Description |
| --- | --- | --- |
| [Archive Folder](actions/archive-folder.md) | PUT | Archives a folder in EARLY. |
| [Create Folder](actions/create-folder.md) | POST | Creates a new folder in EARLY. |
| [Delete Folder](actions/delete-folder.md) | DELETE | Deletes a folder from EARLY. |
| [Get Folder](actions/get-folder.md) | GET | Retrieves a folder from EARLY. |
| [List Folders](actions/list-folders.md) | GET | Retrieves folders from EARLY. |
| [Unarchive Folder](actions/unarchive-folder.md) | PUT | Unarchives a folder in EARLY. |
| [Update Folder](actions/update-folder.md) | PUT | Updates a folder in EARLY. |

### Folder Member

| Action | Method | Description |
| --- | --- | --- |
| [Add Member to Folder](actions/add-member-to-folder.md) | POST | Adds a member to an EARLY folder. |
| [Get Folder Member](actions/get-folder-member.md) | GET | Retrieves a folder member from EARLY. |
| [List Folder Members](actions/list-folder-members.md) | GET | Retrieves members in an EARLY folder. |
| [Remove Member from Folder](actions/remove-member-from-folder.md) | DELETE | Removes a member from an EARLY folder. |

### Leave

| Action | Method | Description |
| --- | --- | --- |
| [Approve Leave](actions/approve-leave.md) | PUT | Approves a leave in EARLY. |
| [Create Leave](actions/create-leave.md) | POST | Creates a new leave in EARLY. |
| [Create Leave for User](actions/create-leave-for-user.md) | POST | Creates a leave in EARLY for a user. |
| [Delete Leave](actions/delete-leave.md) | DELETE | Deletes a leave from EARLY. |
| [Deny Leave](actions/deny-leave.md) | PUT | Denies a leave in EARLY. |
| [List Leaves](actions/list-leaves.md) | GET | Retrieves leaves from EARLY. |

### Leave Type

| Action | Method | Description |
| --- | --- | --- |
| [List Leave Types](actions/list-leave-types.md) | GET | Retrieves leave types from EARLY. |

### Mention

| Action | Method | Description |
| --- | --- | --- |
| [Create Mention](actions/create-mention.md) | POST | Creates a new mention in EARLY. |
| [Delete Mention](actions/delete-mention.md) | DELETE | Deletes a mention from EARLY. |
| [Update Mention](actions/update-mention.md) | PUT | Updates a mention in EARLY. |

### Report

| Action | Method | Description |
| --- | --- | --- |
| [Generate Report](actions/generate-report.md) | GET | Generates a report in EARLY. |

### Tag

| Action | Method | Description |
| --- | --- | --- |
| [Create Tag](actions/create-tag.md) | POST | Creates a new tag in EARLY. |
| [Delete Tag](actions/delete-tag.md) | DELETE | Deletes a tag from EARLY. |
| [Update Tag](actions/update-tag.md) | PUT | Updates a tag in EARLY. |

### Tag And Mention

| Action | Method | Description |
| --- | --- | --- |
| [List Tags and Mentions](actions/list-tags-and-mentions.md) | GET | Retrieves tags and mentions from EARLY. |

### Time Entry

| Action | Method | Description |
| --- | --- | --- |
| [Create Time Entry](actions/create-time-entry.md) | POST | Creates a new time entry in EARLY. |
| [Delete Time Entry](actions/delete-time-entry.md) | DELETE | Deletes a time entry from EARLY. |
| [Get Time Entry](actions/get-time-entry.md) | GET | Retrieves a time entry from EARLY. |
| [List Time Entries in Range](actions/list-time-entries-in-range.md) | GET | Retrieves time entries from EARLY in a date range. |
| [Stop Tracking](actions/stop-tracking.md) | POST | Stops the current tracking session in EARLY. |
| [Update Time Entry](actions/update-time-entry.md) | PUT | Updates a time entry in EARLY. |

### Tracking

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Tracking](actions/cancel-tracking.md) | DELETE | Cancels the current tracking session in EARLY. |
| [Get Current Tracking](actions/get-current-tracking.md) | GET | Retrieves the current tracking session from EARLY. |
| [Start Tracking](actions/start-tracking.md) | POST | Starts time tracking in EARLY for an activity. |
| [Update Tracking](actions/update-tracking.md) | PUT | Updates the current tracking session in EARLY. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | GET | Retrieves the current user from EARLY. |
| [List Users](actions/list-users.md) | GET | Retrieves users from EARLY. |

### Webhook Event

| Action | Method | Description |
| --- | --- | --- |
| [List available Webhook Events](actions/list-available-webhook-events.md) | GET | Retrieves available webhook events from EARLY. |

### Webhook Subscription

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook Subscription](actions/create-webhook-subscription.md) | POST | Creates a webhook subscription in EARLY. |
| [Delete Webhook Subscription](actions/delete-webhook-subscription.md) | DELETE | Deletes a webhook subscription from EARLY. |
| [Delete Webhook Subscriptions for User](actions/delete-webhook-subscriptions-for-user.md) | DELETE | Deletes webhook subscriptions in EARLY for a user. |
| [List Webhook Subscriptions](actions/list-webhook-subscriptions.md) | GET | Retrieves webhook subscriptions from EARLY. |

