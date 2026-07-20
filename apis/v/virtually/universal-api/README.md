# <img src="https://images.mindcloud.co/apps/icons/virtually_1775060535945.png" alt="Virtually logo" width="28" height="28"> Virtually: Universal API

Manage members, events, and attendance with Virtually

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/virtually/latest
- **Category:** Marketing / Events & Webinars
- **Actions:** 31
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://tryvirtually.com/
- **Vendor API docs:** https://app.tryvirtually.com/api/docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Organization](actions/get-organization.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/virtually/latest/actions/get-organization?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (31)

### Action

| Action | Method | Description |
| --- | --- | --- |
| [Create Action](actions/create-action.md) | POST | Creates a new action in Virtually. |
| [Delete Action](actions/delete-action.md) | DELETE | Deletes an existing action from Virtually. |
| [Get Action](actions/get-action.md) | GET | Retrieves an action from your Virtually workspace. |
| [List Actions](actions/list-actions.md) | GET | Retrieves actions from your Virtually workspace. |
| [Update Action](actions/update-action.md) | PUT | Updates an existing action in Virtually. |

### Activity Feed Entry

| Action | Method | Description |
| --- | --- | --- |
| [List Activity Feed Entries](actions/list-activity-feed-entries.md) | GET | Retrieves activity feed entries from Virtually. |

### Attendance

| Action | Method | Description |
| --- | --- | --- |
| [Get Member Attendance](actions/get-member-attendance.md) | GET | Retrieves a member's attendance from Virtually. |

### Automation

| Action | Method | Description |
| --- | --- | --- |
| [Create Automation](actions/create-automation.md) | POST | Creates a new automation in Virtually. |
| [Delete Automation](actions/delete-automation.md) | DELETE | Deletes an existing automation from Virtually. |
| [Get Automation](actions/get-automation.md) | GET | Retrieves an automation from your Virtually workspace. |
| [List Automations](actions/list-automations.md) | GET | Retrieves automations from your Virtually workspace. |
| [Update Automation](actions/update-automation.md) | PUT | Updates an existing automation in Virtually. |

### Custom Data Key

| Action | Method | Description |
| --- | --- | --- |
| [List Custom Data Keys](actions/list-custom-data-keys.md) | GET | Retrieves custom data event keys from Virtually. |

### Custom Data Record

| Action | Method | Description |
| --- | --- | --- |
| [Create Custom Data Record](actions/create-custom-data-record.md) | POST | Creates a new custom data record in Virtually. |
| [List Custom Data Records](actions/list-custom-data-records.md) | GET | Retrieves custom data records from Virtually. |

### Member

| Action | Method | Description |
| --- | --- | --- |
| [Create Member](actions/create-member.md) | POST | Creates a new member in Virtually. |
| [Delete Member](actions/delete-member.md) | DELETE | Deletes an existing member from Virtually. |
| [Get Member](actions/get-member.md) | GET | Retrieves a member from your Virtually workspace. |
| [List Members](actions/list-members.md) | GET | Retrieves members from your Virtually workspace. |
| [Update Member](actions/update-member.md) | PUT | Updates an existing member in Virtually. |

### Organization

| Action | Method | Description |
| --- | --- | --- |
| [Get Organization](actions/get-organization.md) | GET | Retrieves organization details from your Virtually workspace. |

### Report

| Action | Method | Description |
| --- | --- | --- |
| [List Reports](actions/list-reports.md) | GET | Retrieves reports from your Virtually workspace. |

### Report Summary

| Action | Method | Description |
| --- | --- | --- |
| [Get Report Summary](actions/get-report-summary.md) | GET | Retrieves a report summary from Virtually. |

### Sender Profile

| Action | Method | Description |
| --- | --- | --- |
| [List Sender Profiles](actions/list-sender-profiles.md) | GET | Retrieves sender profiles for a platform from Virtually. |

### Tag

| Action | Method | Description |
| --- | --- | --- |
| [List Member Tags](actions/list-member-tags.md) | GET | Retrieves member tags from your Virtually workspace. |
| [Upsert Tags](actions/upsert-tags.md) | PUT | Creates or updates tags in Virtually. |

### Trigger

| Action | Method | Description |
| --- | --- | --- |
| [Create Trigger](actions/create-trigger.md) | POST | Creates a new trigger in Virtually. |
| [Delete Trigger](actions/delete-trigger.md) | DELETE | Deletes an existing trigger from Virtually. |
| [Get Trigger](actions/get-trigger.md) | GET | Retrieves a trigger from your Virtually workspace. |
| [List Triggers](actions/list-triggers.md) | GET | Retrieves triggers from your Virtually workspace. |
| [Update Trigger](actions/update-trigger.md) | PUT | Updates an existing trigger in Virtually. |

