# <img src="https://images.mindcloud.co/apps/icons/rotacloud-icon_1776113204130.png" alt="RotaCloud logo" width="28" height="28"> RotaCloud: Universal API

RotaCloud API integration for workforce scheduling, leave, attendance, users, shifts, and related admin operations.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/rotaCloud/latest
- **Category:** Productivity / Scheduling
- **Actions:** 126
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://rotacloud.com
- **Vendor API docs:** https://help.rotacloud.com/en/articles/2987763-custom-integrations-using-the-rotacloud-api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Accounts](actions/list-accounts.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rotaCloud/latest/actions/list-accounts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (126)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Get Account](actions/get-account.md) | GET |  |
| [List Accounts](actions/list-accounts.md) | GET | Lists accounts in RotaCloud. |

### Active Terminal

| Action | Method | Description |
| --- | --- | --- |
| [Close Active Terminal](actions/close-active-terminal.md) | DELETE |  |
| [Launch Active Terminal](actions/launch-active-terminal.md) | POST | Launches a terminal in RotaCloud. |
| [List Active Terminals](actions/list-active-terminals.md) | GET | Lists active terminals in RotaCloud. |
| [Ping Active Terminal](actions/ping-active-terminal.md) | PUT | Pings an active terminal in RotaCloud. |

### Attendance Record

| Action | Method | Description |
| --- | --- | --- |
| [Create Attendance Record](actions/create-attendance-record.md) | POST | Creates an attendance record in RotaCloud. |
| [Delete Attendance Record](actions/delete-attendance-record.md) | DELETE | Deletes an attendance record from RotaCloud. |
| [Get Attendance Record](actions/get-attendance-record.md) | GET | Retrieves an attendance record from RotaCloud. |
| [List Attendance Records](actions/list-attendance-records.md) | GET | Lists attendance records in RotaCloud. |
| [Update Attendance Record](actions/update-attendance-record.md) | PUT | Updates an attendance record in RotaCloud. |

### Auth Context

| Action | Method | Description |
| --- | --- | --- |
| [List Auth Context](actions/list-auth-context.md) | GET |  |

### Availability

| Action | Method | Description |
| --- | --- | --- |
| [Create Availability](actions/create-availability.md) | POST | Creates availability in RotaCloud. |
| [Delete Availability](actions/delete-availability.md) | DELETE |  |
| [List Availability](actions/list-availability.md) | GET | Retrieves availability from RotaCloud. |
| [Update Availability](actions/update-availability.md) | PUT |  |

### Clocked In User

| Action | Method | Description |
| --- | --- | --- |
| [Clock In User](actions/clock-in-user.md) | POST |  |
| [Clock Out User](actions/clock-out-user.md) | PUT |  |
| [Get Clocked In User](actions/get-clocked-in-user.md) | GET | Retrieves a clocked in user from RotaCloud. |
| [List Clocked In Users](actions/list-clocked-in-users.md) | GET | Lists clocked in users in RotaCloud. |

### Daily Budget

| Action | Method | Description |
| --- | --- | --- |
| [List Daily Budgets](actions/list-daily-budgets.md) | GET |  |
| [Update Daily Budgets Batch](actions/update-daily-budgets-batch.md) | PUT |  |

### Daily Revenue

| Action | Method | Description |
| --- | --- | --- |
| [List Daily Revenue](actions/list-daily-revenue.md) | GET |  |
| [Update Daily Revenue Batch](actions/update-daily-revenue-batch.md) | PUT |  |

### Day Note

| Action | Method | Description |
| --- | --- | --- |
| [Create Day Note](actions/create-day-note.md) | POST | Creates a day note in RotaCloud. |
| [Create Day Note V2](actions/create-day-note-v2.md) | POST |  |
| [Delete Day Note](actions/delete-day-note.md) | DELETE | Deletes a day note from RotaCloud. |
| [Delete Day Note V2](actions/delete-day-note-v2.md) | DELETE |  |
| [Get Day Note](actions/get-day-note.md) | GET | Retrieves a day note from RotaCloud. |
| [Get Day Note V2](actions/get-day-note-v2.md) | GET |  |
| [List Day Notes](actions/list-day-notes.md) | GET | Lists day notes in RotaCloud. |
| [List Day Notes V2](actions/list-day-notes-v2.md) | GET |  |
| [Update Day Note](actions/update-day-note.md) | PUT | Updates a day note in RotaCloud. |
| [Update Day Note V2](actions/update-day-note-v2.md) | PUT |  |

### Day Off

| Action | Method | Description |
| --- | --- | --- |
| [Create Day Off](actions/create-day-off.md) | POST | Creates days off in RotaCloud. |
| [Delete Day Off](actions/delete-day-off.md) | DELETE |  |
| [List Days Off](actions/list-days-off.md) | GET | Lists days off in RotaCloud. |

### Document

| Action | Method | Description |
| --- | --- | --- |
| [Create Document](actions/create-document.md) | POST | Creates a document in RotaCloud. |
| [Delete Document](actions/delete-document.md) | DELETE | Deletes a document from RotaCloud. |
| [Get Document](actions/get-document.md) | GET |  |
| [List Documents](actions/list-documents.md) | GET | Lists documents in RotaCloud. |
| [Update Document](actions/update-document.md) | PUT | Updates a document in RotaCloud. |

### Group

| Action | Method | Description |
| --- | --- | --- |
| [Create Group](actions/create-group.md) | POST | Creates a group in RotaCloud. |
| [Delete Group](actions/delete-group.md) | DELETE | Deletes a group from RotaCloud. |
| [Get Group](actions/get-group.md) | GET | Retrieves a group from RotaCloud. |
| [List Groups](actions/list-groups.md) | GET | Lists groups in RotaCloud. |
| [Update Group](actions/update-group.md) | PUT | Updates a group in RotaCloud. |

### Invoice

| Action | Method | Description |
| --- | --- | --- |
| [Get Invoice](actions/get-invoice.md) | GET |  |
| [List Invoices](actions/list-invoices.md) | GET |  |

### Leave Embargo

| Action | Method | Description |
| --- | --- | --- |
| [Create Leave Embargo](actions/create-leave-embargo.md) | POST | Creates a leave embargo in RotaCloud. |
| [Delete Leave Embargo](actions/delete-leave-embargo.md) | DELETE | Deletes a leave embargo from RotaCloud. |
| [Get Leave Embargo](actions/get-leave-embargo.md) | GET | Retrieves a leave embargo from RotaCloud. |
| [List Leave Embargoes](actions/list-leave-embargoes.md) | GET | Lists leave embargoes in RotaCloud. |
| [Update Leave Embargo](actions/update-leave-embargo.md) | PUT | Updates a leave embargo in RotaCloud. |

### Leave Entry

| Action | Method | Description |
| --- | --- | --- |
| [Create Leave Entry](actions/create-leave-entry.md) | POST | Creates a leave record in RotaCloud. |
| [Delete Leave Entry](actions/delete-leave-entry.md) | DELETE | Deletes a leave record from RotaCloud. |
| [Get Leave Entry](actions/get-leave-entry.md) | GET | Retrieves a leave record from RotaCloud. |
| [List Leave Entries](actions/list-leave-entries.md) | GET | Lists leave records in RotaCloud. |
| [Update Leave Entry](actions/update-leave-entry.md) | PUT | Updates a leave record in RotaCloud. |

### Leave Request

| Action | Method | Description |
| --- | --- | --- |
| [Create Leave Request](actions/create-leave-request.md) | POST | Requests leave in RotaCloud. |
| [Delete Leave Request](actions/delete-leave-request.md) | DELETE | Deletes a leave request from RotaCloud. |
| [Get Leave Request](actions/get-leave-request.md) | GET | Retrieves a leave request from RotaCloud. |
| [List Leave Requests](actions/list-leave-requests.md) | GET | Lists leave requests in RotaCloud. |
| [Update Leave Request](actions/update-leave-request.md) | PUT |  |

### Leave Type

| Action | Method | Description |
| --- | --- | --- |
| [List Leave Types](actions/list-leave-types.md) | GET | Lists leave types in RotaCloud. |

### Location

| Action | Method | Description |
| --- | --- | --- |
| [Create Location](actions/create-location.md) | POST | Creates a location in RotaCloud. |
| [Delete Location](actions/delete-location.md) | DELETE | Deletes a location from RotaCloud. |
| [Get Location](actions/get-location.md) | GET | Retrieves a location from RotaCloud. |
| [List Locations](actions/list-locations.md) | GET | Lists locations in RotaCloud. |
| [Update Location](actions/update-location.md) | PUT | Updates a location in RotaCloud. |

### Logbook Category

| Action | Method | Description |
| --- | --- | --- |
| [Create Logbook Category](actions/create-logbook-category.md) | POST |  |
| [Delete Logbook Category](actions/delete-logbook-category.md) | DELETE |  |
| [Get Logbook Category](actions/get-logbook-category.md) | GET |  |
| [List Logbook Categories](actions/list-logbook-categories.md) | GET |  |
| [Update Logbook Category](actions/update-logbook-category.md) | PUT |  |

### Logbook Entry

| Action | Method | Description |
| --- | --- | --- |
| [Create Logbook Entry](actions/create-logbook-entry.md) | POST |  |
| [Delete Logbook Entry](actions/delete-logbook-entry.md) | DELETE |  |
| [Get Logbook Entry](actions/get-logbook-entry.md) | GET |  |
| [List Logbook Entries](actions/list-logbook-entries.md) | GET |  |
| [Update Logbook Entry](actions/update-logbook-entry.md) | PUT |  |

### Message

| Action | Method | Description |
| --- | --- | --- |
| [List Messages](actions/list-messages.md) | GET | Lists your messages in RotaCloud. |
| [Send Message](actions/send-message.md) | POST | Sends a message in RotaCloud. |

### Onboarding Link

| Action | Method | Description |
| --- | --- | --- |
| [Resend Onboarding Link](actions/resend-onboarding-link.md) | POST |  |

### Onboarding Request

| Action | Method | Description |
| --- | --- | --- |
| [Create Onboarding Request](actions/create-onboarding-request.md) | POST |  |
| [Update User Onboarding](actions/update-user-onboarding.md) | PUT |  |

### Pin

| Action | Method | Description |
| --- | --- | --- |
| [Get Pin](actions/get-pin.md) | GET |  |

### Role

| Action | Method | Description |
| --- | --- | --- |
| [Create Role](actions/create-role.md) | POST | Creates a role in RotaCloud. |
| [Delete Role](actions/delete-role.md) | DELETE | Deletes a role from RotaCloud. |
| [Get Role](actions/get-role.md) | GET | Retrieves a role from RotaCloud. |
| [List Roles](actions/list-roles.md) | GET | Lists roles in RotaCloud. |
| [Update Role](actions/update-role.md) | PUT | Updates a role in RotaCloud. |

### Setting

| Action | Method | Description |
| --- | --- | --- |
| [List Settings](actions/list-settings.md) | GET | Lists account settings in RotaCloud. |

### Shift

| Action | Method | Description |
| --- | --- | --- |
| [Acknowledge Shifts](actions/acknowledge-shifts.md) | PUT | Acknowledges shifts in RotaCloud. |
| [Create Shift](actions/create-shift.md) | POST | Creates a shift in RotaCloud. |
| [Delete Shift](actions/delete-shift.md) | DELETE | Deletes a shift from RotaCloud. |
| [Delete Shifts Batch](actions/delete-shifts-batch.md) | DELETE |  |
| [Get Shift](actions/get-shift.md) | GET | Retrieves a shift from RotaCloud. |
| [List Shifts](actions/list-shifts.md) | GET | Lists shifts in RotaCloud. |
| [Publish Shifts](actions/publish-shifts.md) | PUT | Publishes shifts in RotaCloud. |
| [Unpublish Shifts](actions/unpublish-shifts.md) | DELETE | Unpublishes shifts in RotaCloud. |
| [Update Shift](actions/update-shift.md) | PUT | Updates a shift in RotaCloud. |
| [Update Shifts Batch](actions/update-shifts-batch.md) | PUT |  |

### Shift Drop Request

| Action | Method | Description |
| --- | --- | --- |
| [Update Shift Drop Request](actions/update-shift-drop-request.md) | PUT |  |

### Shift History Record

| Action | Method | Description |
| --- | --- | --- |
| [Get Shift History](actions/get-shift-history.md) | GET |  |

### Shift Swap Request

| Action | Method | Description |
| --- | --- | --- |
| [Update Shift Swap Request](actions/update-shift-swap-request.md) | PUT |  |

### Terminal

| Action | Method | Description |
| --- | --- | --- |
| [Close Terminal](actions/close-terminal.md) | DELETE | Closes a terminal in RotaCloud. |
| [Create Terminal](actions/create-terminal.md) | POST | Creates a terminal in RotaCloud. |
| [Get Terminal](actions/get-terminal.md) | GET | Retrieves a terminal from RotaCloud. |
| [List Terminals](actions/list-terminals.md) | GET | Lists terminals in RotaCloud. |
| [Update Terminal](actions/update-terminal.md) | PUT | Updates a terminal in RotaCloud. |

### Timezone

| Action | Method | Description |
| --- | --- | --- |
| [Get Timezone](actions/get-timezone.md) | GET | Retrieves a timezone from RotaCloud. |
| [List Timezones](actions/list-timezones.md) | GET | Lists timezones in RotaCloud. |

### Toil Accrual

| Action | Method | Description |
| --- | --- | --- |
| [Create TOIL Accrual](actions/create-toil-accrual.md) | POST | Creates a toil accrual record in RotaCloud. |
| [Delete TOIL Accrual](actions/delete-toil-accrual.md) | DELETE | Deletes a toil accrual record from RotaCloud. |
| [Get Toil Accrual](actions/get-toil-accrual.md) | GET | Retrieves a toil accrual record from RotaCloud. |
| [List Toil Accruals](actions/list-toil-accruals.md) | GET | Lists toil accruals in RotaCloud. |

### Toil Allowance

| Action | Method | Description |
| --- | --- | --- |
| [List Toil Allowance](actions/list-toil-allowance.md) | GET |  |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Create User](actions/create-user.md) | POST | Creates a user in RotaCloud. |
| [Create Users Onboarding Batch V2](actions/create-users-onboarding-batch-v2.md) | POST |  |
| [Create Users V2](actions/create-users-v2.md) | POST |  |
| [Delete User](actions/delete-user.md) | DELETE | Deletes a user from RotaCloud. |
| [Get User](actions/get-user.md) | GET | Retrieves a user from RotaCloud. |
| [List Users](actions/list-users.md) | GET | Lists users in RotaCloud. |
| [Update User](actions/update-user.md) | PUT | Updates a user in RotaCloud. |

### User Break

| Action | Method | Description |
| --- | --- | --- |
| [End User Break](actions/end-user-break.md) | PUT | Ends a user's break in RotaCloud. |
| [Start User Break](actions/start-user-break.md) | PUT |  |

