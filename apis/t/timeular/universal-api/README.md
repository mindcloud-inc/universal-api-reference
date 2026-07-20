# <img src="https://images.mindcloud.co/apps/icons/early-timeular-icon-512_1776353394635.png" alt="Timeular logo" width="28" height="28"> Timeular: Universal API

Timeular (EARLY) is a time tracking and leave management platform with activity, folder, time entry, reporting, leave, user, and webhook APIs.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/timeular/latest
- **Category:** Human Resources / HRIS
- **Actions:** 113
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://early.app
- **Vendor API docs:** https://developers.early.app

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Generate Report](actions/generate-report.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/timeular/latest/actions/generate-report?connectionId=$CONNECTION_ID&date=string&fileType=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (113)

### Activities

| Action | Method | Description |
| --- | --- | --- |
| [V2 Archive an Activity](actions/v2-archive-an-activity.md) | DELETE | Deletes an activity from the Timeular v2 API. |
| [V2 Assign an Activity to Device Side](actions/v2-assign-an-activity-to-device-side.md) | PUT | Assigns an activity to a device side in the Timeular v2 API. |
| [V2 Create an Activity](actions/v2-create-an-activity.md) | POST | Creates a new activity in the Timeular v2 API. |
| [V2 Edit an Activity](actions/v2-edit-an-activity.md) | PUT | Updates an existing activity in the Timeular v2 API. |
| [V2 List all Activities](actions/v2-list-all-activities.md) | GET | Retrieves activities from the Timeular v2 API. |
| [V2 List all Archived Activities](actions/v2-list-all-archived-activities.md) | GET | Retrieves archived activities from the Timeular v2 API. |
| [V2 Unassign an Activity from a Device Side](actions/v2-unassign-an-activity-from-a-device-side.md) | DELETE | Removes an activity from a device side in the Timeular v2 API. |
| [V3 Archive an Activity](actions/v3-archive-an-activity.md) | DELETE | Deletes an activity from the Timeular v3 API. |
| [V3 Assign an Activity to Device Side](actions/v3-assign-an-activity-to-device-side.md) | PUT | Assigns an activity to a device side in the Timeular v3 API. |
| [V3 Create an Activity](actions/v3-create-an-activity.md) | POST | Creates a new activity in the Timeular v3 API. |
| [V3 Edit an Activity](actions/v3-edit-an-activity.md) | PUT | Updates an existing activity in the Timeular v3 API. |
| [V3 List all Activities](actions/v3-list-all-activities.md) | GET | Retrieves activities from the Timeular v3 API. |
| [V3 Unassign an Activity from a Device Side](actions/v3-unassign-an-activity-from-a-device-side.md) | DELETE | Removes an activity from a device side in the Timeular v3 API. |

### Activity

| Action | Method | Description |
| --- | --- | --- |
| [Archive Activity](actions/archive-activity.md) | DELETE | Deletes an activity from your Timeular workspace. |
| [Create Activity](actions/create-activity.md) | POST | Creates a new activity in your Timeular workspace. |
| [List Activities](actions/list-activities.md) | GET | Retrieves activities from your Timeular workspace. |
| [Unarchive Activity](actions/unarchive-activity.md) | PUT | Unarchives an existing activity in your Timeular workspace. |
| [Update Activity](actions/update-activity.md) | PUT | Updates an existing activity in your Timeular workspace. |

### Folder

| Action | Method | Description |
| --- | --- | --- |
| [Archive Folder](actions/archive-folder.md) | PUT | Archives an existing folder in your Timeular workspace. |
| [Create Folder](actions/create-folder.md) | POST | Creates a new folder in your Timeular workspace. |
| [Delete Folder](actions/delete-folder.md) | DELETE | Deletes a folder from your Timeular workspace. |
| [Get Folder](actions/get-folder.md) | GET | Retrieves a folder from your Timeular workspace. |
| [List Folders](actions/list-folders.md) | GET | Retrieves folders from your Timeular workspace. |
| [Unarchive Folder](actions/unarchive-folder.md) | PUT | Unarchives an existing folder in your Timeular workspace. |
| [Update Folder](actions/update-folder.md) | PUT | Updates an existing folder in your Timeular workspace. |

### Folder Member

| Action | Method | Description |
| --- | --- | --- |
| [Add Member to Folder](actions/add-member-to-folder.md) | POST | Adds a member to a folder in your Timeular workspace. |
| [Get Folder Member](actions/get-folder-member.md) | GET | Retrieves a folder member from your Timeular workspace. |
| [List Folder Members](actions/list-folder-members.md) | GET | Retrieves members for a folder in your Timeular workspace. |
| [Remove Member from Folder](actions/remove-member-from-folder.md) | DELETE | Removes a member from a folder in your Timeular workspace. |

### Leave

| Action | Method | Description |
| --- | --- | --- |
| [Approve Leave](actions/approve-leave.md) | PUT | Approves a leave request in your Timeular workspace. |
| [Create Leave](actions/create-leave.md) | POST | Creates a new leave request in your Timeular workspace. |
| [Create Leave for User](actions/create-leave-for-user.md) | POST | Creates a leave request for a user in your Timeular workspace. |
| [Delete Leave](actions/delete-leave.md) | DELETE | Deletes a leave request from your Timeular workspace. |
| [Deny Leave](actions/deny-leave.md) | PUT | Denies a leave request in your Timeular workspace. |
| [List Leaves](actions/list-leaves.md) | GET | Retrieves leave requests from your Timeular workspace. |

### Leave Type

| Action | Method | Description |
| --- | --- | --- |
| [List Leave Types](actions/list-leave-types.md) | GET | Retrieves leave types from your Timeular workspace. |

### Mention

| Action | Method | Description |
| --- | --- | --- |
| [Create Mention](actions/create-mention.md) | POST | Creates a new mention in your Timeular workspace. |
| [Delete Mention](actions/delete-mention.md) | DELETE | Deletes a mention from your Timeular workspace. |
| [Update Mention](actions/update-mention.md) | PUT | Updates an existing mention in your Timeular workspace. |

### Report

| Action | Method | Description |
| --- | --- | --- |
| [Generate Report](actions/generate-report.md) | GET | Generates a time entry report in your Timeular workspace. |

### Tag

| Action | Method | Description |
| --- | --- | --- |
| [Create Tag](actions/create-tag.md) | POST | Creates a new tag in your Timeular workspace. |
| [Delete Tag](actions/delete-tag.md) | DELETE | Deletes a tag from your Timeular workspace. |
| [Update Tag](actions/update-tag.md) | PUT | Updates an existing tag in your Timeular workspace. |

### Tag And Mention

| Action | Method | Description |
| --- | --- | --- |
| [List Tags and Mentions](actions/list-tags-and-mentions.md) | GET | Retrieves tags and mentions from your Timeular workspace. |

### Tags

| Action | Method | Description |
| --- | --- | --- |
| [V3 Create Tag](actions/v3-create-tag.md) | POST | Creates a new tag in the Timeular v3 API. |
| [V3 Delete Tag](actions/v3-delete-tag.md) | DELETE | Deletes a tag from the Timeular v3 API. |
| [V3 Update Tag](actions/v3-update-tag.md) | PUT | Updates an existing tag in the Timeular v3 API. |

### Time Entry

| Action | Method | Description |
| --- | --- | --- |
| [Create Time Entry](actions/create-time-entry.md) | POST | Creates a new time entry in your Timeular workspace. |
| [Delete Time Entry](actions/delete-time-entry.md) | DELETE | Deletes a time entry from your Timeular workspace. |
| [Get Time Entry](actions/get-time-entry.md) | GET | Retrieves a time entry from your Timeular workspace. |
| [List Time Entries in Range](actions/list-time-entries-in-range.md) | GET | Retrieves time entries in a date range from your Timeular workspace. |
| [Stop Tracking](actions/stop-tracking.md) | POST | Creates a time entry by stopping tracking in your Timeular workspace. |
| [Update Time Entry](actions/update-time-entry.md) | PUT | Updates an existing time entry in your Timeular workspace. |

### Timesheet Entries

| Action | Method | Description |
| --- | --- | --- |
| [V2 Create Time Entry](actions/v2-create-time-entry.md) | POST | Creates a new time entry in the Timeular v2 API. |
| [V2 Delete Time Entry](actions/v2-delete-time-entry.md) | DELETE | Deletes a time entry from the Timeular v2 API. |
| [V2 Edit Time Entry](actions/v2-edit-time-entry.md) | PUT | Updates an existing time entry in the Timeular v2 API. |
| [V2 Edit Tracking](actions/v2-edit-tracking.md) | PUT | Updates the current tracking session in the Timeular v2 API. |
| [V2 Find Time Entries in given range](actions/v2-find-time-entries-in-given-range.md) | GET | Retrieves time entries in a date range from the Timeular v2 API. |
| [V2 Find Time Entry](actions/v2-find-time-entry.md) | GET | Retrieves a time entry from the Timeular v2 API. |
| [V2 Show current Tracking](actions/v2-show-current-tracking.md) | GET | Retrieves the current tracking session from the Timeular v2 API. |
| [V2 Start Tracking](actions/v2-start-tracking.md) | POST | Creates a tracking session in the Timeular v2 API. |
| [V2 Stop Tracking](actions/v2-stop-tracking.md) | POST | Creates a time entry by stopping tracking in the Timeular v2 API. |
| [V3 Create Time Entry](actions/v3-create-time-entry.md) | POST | Creates a new time entry in the Timeular v3 API. |
| [V3 Delete a Time Entry](actions/v3-delete-a-time-entry.md) | DELETE | Deletes a time entry from the Timeular v3 API. |
| [V3 Edit a Time Entry](actions/v3-edit-a-time-entry.md) | PUT | Updates an existing time entry in the Timeular v3 API. |
| [V3 Edit Tracking](actions/v3-edit-tracking.md) | PUT | Updates the current tracking session in the Timeular v3 API. |
| [V3 Find Time Entries in given range](actions/v3-find-time-entries-in-given-range.md) | GET | Retrieves time entries in a date range from the Timeular v3 API. |
| [V3 Find Time Entry by its ID](actions/v3-find-time-entry-by-its-id.md) | GET | Retrieves a time entry by ID from the Timeular v3 API. |
| [V3 Show current Tracking](actions/v3-show-current-tracking.md) | GET | Retrieves the current tracking session from the Timeular v3 API. |
| [V3 Start Tracking](actions/v3-start-tracking.md) | POST | Creates a tracking session in the Timeular v3 API. |
| [V3 Stop Tracking](actions/v3-stop-tracking.md) | POST | Creates a time entry by stopping tracking in the Timeular v3 API. |

### Tracking

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Tracking](actions/cancel-tracking.md) | DELETE | Deletes the current tracking session from your Timeular workspace. |
| [Get Current Tracking](actions/get-current-tracking.md) | GET | Retrieves the current tracking session from your Timeular workspace. |
| [Start Tracking](actions/start-tracking.md) | POST | Creates a tracking session in your Timeular workspace. |
| [Update Tracking](actions/update-tracking.md) | PUT | Updates the current tracking session in your Timeular workspace. |

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [V2 Disable a Device](actions/v2-disable-a-device.md) | PUT | Disables a device in the Timeular v2 API. |
| [V2 Edit a Device](actions/v2-edit-a-device.md) | PUT | Updates an existing device in the Timeular v2 API. |
| [V2 Enable a Device](actions/v2-enable-a-device.md) | DELETE | Enables a device in the Timeular v2 API. |
| [V2 Fetch Tags & Mentions](actions/v2-fetch-tags-mentions.md) | GET | Retrieves tags and mentions from the Timeular v2 API. |
| [V2 Generate Report](actions/v2-generate-report.md) | GET | Generates a time entry report in the Timeular v2 API. |
| [V2 List all known Devices](actions/v2-list-all-known-devices.md) | GET | Retrieves devices from the Timeular v2 API. |
| [V2 List enabled Integrations](actions/v2-list-enabled-integrations.md) | GET | Retrieves enabled integrations from the Timeular v2 API. |
| [V2 Remove known Device](actions/v2-remove-known-device.md) | DELETE | Deletes a device from the Timeular v2 API. |
| [V2 Removes the active status from the given Device](actions/v2-removes-the-active-status-from-the-given-device.md) | DELETE | Removes active status from a device in the Timeular v2 API. |
| [V2 Sets the status of a Device to active](actions/v2-sets-the-status-of-a-device-to-active.md) | POST | Sets a device as active in the Timeular v2 API. |
| [V3 Activate Device](actions/v3-activate-device.md) | PUT | Activates a device in the Timeular v3 API. |
| [V3 All Data as JSON](actions/v3-all-data-as-json.md) | GET | Retrieves report data as JSON from the Timeular v3 API. |
| [V3 Create Mention](actions/v3-create-mention.md) | POST | Creates a new mention in the Timeular v3 API. |
| [V3 Deactivate Device](actions/v3-deactivate-device.md) | PUT | Deactivates a device in the Timeular v3 API. |
| [V3 Delete Mention](actions/v3-delete-mention.md) | DELETE | Deletes a mention from the Timeular v3 API. |
| [V3 Disable Device](actions/v3-disable-device.md) | PUT | Disables a device in the Timeular v3 API. |
| [V3 Edit Device](actions/v3-edit-device.md) | PUT | Updates an existing device in the Timeular v3 API. |
| [V3 Enable Device](actions/v3-enable-device.md) | PUT | Enables a device in the Timeular v3 API. |
| [V3 Fetch Tags & Mentions](actions/v3-fetch-tags-mentions.md) | GET | Retrieves tags and mentions from the Timeular v3 API. |
| [V3 Forget Device](actions/v3-forget-device.md) | DELETE | Deletes a device from the Timeular v3 API. |
| [V3 Generate Report](actions/v3-generate-report.md) | GET | Generates a time entry report in the Timeular v3 API. |
| [V3 List all known Devices](actions/v3-list-all-known-devices.md) | GET | Retrieves devices from the Timeular v3 API. |
| [V3 List enabled Integrations](actions/v3-list-enabled-integrations.md) | GET | Retrieves enabled integrations from the Timeular v3 API. |
| [V3 Spaces with Members](actions/v3-spaces-with-members.md) | GET | Retrieves spaces with members from the Timeular v3 API. |
| [V3 Update Mention](actions/v3-update-mention.md) | PUT | Updates an existing mention in the Timeular v3 API. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | GET | Retrieves the current user from your Timeular workspace. |
| [List Users](actions/list-users.md) | GET | Retrieves users from your Timeular workspace. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [V3 Me](actions/v3-me.md) | GET | Retrieves the current user from the Timeular v3 API. |

### Webhook Endpoints

| Action | Method | Description |
| --- | --- | --- |
| [V3 List Subscriptions](actions/v3-list-subscriptions.md) | GET | Retrieves webhook subscriptions from the Timeular v3 API. |
| [V3 Subscribe](actions/v3-subscribe.md) | POST | Creates a new webhook subscription in the Timeular v3 API. |
| [V3 Unsubscribe](actions/v3-unsubscribe.md) | DELETE | Deletes a webhook subscription from the Timeular v3 API. |
| [V3 Unsubscribe all for User](actions/v3-unsubscribe-all-for-user.md) | DELETE | Deletes current-user webhook subscriptions from the Timeular v3 API. |

### Webhook Event

| Action | Method | Description |
| --- | --- | --- |
| [List available Webhook Events](actions/list-available-webhook-events.md) | GET | Retrieves available webhook events from your Timeular workspace. |

### Webhook Events

| Action | Method | Description |
| --- | --- | --- |
| [V3 List available events](actions/v3-list-available-events.md) | GET | Retrieves available webhook events from the Timeular v3 API. |

### Webhook Subscription

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook Subscription](actions/create-webhook-subscription.md) | POST | Creates a new webhook subscription in your Timeular workspace. |
| [Delete Webhook Subscription](actions/delete-webhook-subscription.md) | DELETE | Deletes a webhook subscription from your Timeular workspace. |
| [Delete Webhook Subscriptions for User](actions/delete-webhook-subscriptions-for-user.md) | DELETE | Deletes current-user webhook subscriptions from your Timeular workspace. |
| [List Webhook Subscriptions](actions/list-webhook-subscriptions.md) | GET | Retrieves webhook subscriptions from your Timeular workspace. |

