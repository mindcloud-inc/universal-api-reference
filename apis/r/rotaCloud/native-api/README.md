# RotaCloud: Native API Reference

A consolidated summary of RotaCloud's API configuration and 126 documented operations, with links to official documentation.

- **Official docs:** https://help.rotacloud.com/en/articles/2987763-custom-integrations-using-the-rotacloud-api/
- **API base URL:** `https://api.rotacloud.com`

## Authentication

### API Key

RotaCloud API key sent as a bearer token in the Authorization header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://help.rotacloud.com/en/articles/2987763-custom-integrations-using-the-rotacloud-api/)

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (126 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Acknowledge Shifts](actions/acknowledge-shifts.md) | `POST /v1/shifts_acknowledged` | [docs](https://rotacloud.com/api/) |
| [Clock In User](actions/clock-in-user.md) | `POST /v1/users_clocked_in/:id` | [docs](https://rotacloud.com/api/) |
| [Clock Out User](actions/clock-out-user.md) | `POST /v1/users_clocked_in/:id` | [docs](https://rotacloud.com/api/) |
| [Close Active Terminal](actions/close-active-terminal.md) | `DELETE /v1/terminals_active/:id` | [docs](https://rotacloud.com/api/) |
| [Close Terminal](actions/close-terminal.md) | `DELETE /v1/terminals/:id` | [docs](https://rotacloud.com/api/) |
| [Create Attendance Record](actions/create-attendance-record.md) | `POST /v1/attendance` | [docs](https://rotacloud.com/api/) |
| [Create Availability](actions/create-availability.md) | `POST /v1/availability` | [docs](https://rotacloud.com/api/) |
| [Create Day Note](actions/create-day-note.md) | `POST /v1/day_notes` | [docs](https://rotacloud.com/api/) |
| [Create Day Note V2](actions/create-day-note-v2.md) | `POST /v2/dayNotes` | [docs](https://rotacloud.com/api/) |
| [Create Day Off](actions/create-day-off.md) | `POST /v1/days_off` | [docs](https://rotacloud.com/api/) |
| [Create Document](actions/create-document.md) | `POST /v1/documents` | [docs](https://rotacloud.com/api/) |
| [Create Group](actions/create-group.md) | `POST /v1/groups` | [docs](https://rotacloud.com/api/) |
| [Create Leave Embargo](actions/create-leave-embargo.md) | `POST /v1/leave_embargoes` | [docs](https://rotacloud.com/api/) |
| [Create Leave Entry](actions/create-leave-entry.md) | `POST /v1/leave` | [docs](https://rotacloud.com/api/) |
| [Create Leave Request](actions/create-leave-request.md) | `POST /v1/leave_requests` | [docs](https://rotacloud.com/api/) |
| [Create Location](actions/create-location.md) | `POST /v1/locations` | [docs](https://rotacloud.com/api/) |
| [Create Logbook Category](actions/create-logbook-category.md) | `POST /v2/logbook/categories` | [docs](https://rotacloud.com/api/) |
| [Create Logbook Entry](actions/create-logbook-entry.md) | `POST /v2/logbook` | [docs](https://rotacloud.com/api/) |
| [Create Onboarding Request](actions/create-onboarding-request.md) | `POST /v2/users/onboard` | [docs](https://rotacloud.com/api/) |
| [Create Role](actions/create-role.md) | `POST /v1/roles` | [docs](https://rotacloud.com/api/) |
| [Create Shift](actions/create-shift.md) | `POST /v1/shifts` | [docs](https://rotacloud.com/api/) |
| [Create Terminal](actions/create-terminal.md) | `POST /v1/terminals` | [docs](https://rotacloud.com/api/) |
| [Create TOIL Accrual](actions/create-toil-accrual.md) | `POST /v1/toil_accruals` | [docs](https://rotacloud.com/api/) |
| [Create User](actions/create-user.md) | `POST /v1/users` | [docs](https://rotacloud.com/api/) |
| [Create Users Onboarding Batch V2](actions/create-users-onboarding-batch-v2.md) | `POST /v2/users` | [docs](https://rotacloud.com/api/) |
| [Create Users V2](actions/create-users-v2.md) | `POST /v2/users` | [docs](https://rotacloud.com/api/) |
| [Delete Attendance Record](actions/delete-attendance-record.md) | `DELETE /v1/attendance/:id` | [docs](https://rotacloud.com/api/) |
| [Delete Availability](actions/delete-availability.md) | `POST /v1/availability` | [docs](https://rotacloud.com/api/) |
| [Delete Day Note](actions/delete-day-note.md) | `DELETE /v1/day_notes/:id` | [docs](https://rotacloud.com/api/) |
| [Delete Day Note V2](actions/delete-day-note-v2.md) | `DELETE /v2/dayNotes/:id` | [docs](https://rotacloud.com/api/) |
| [Delete Day Off](actions/delete-day-off.md) | `DELETE /v1/days_off/:id` | [docs](https://rotacloud.com/api/) |
| [Delete Document](actions/delete-document.md) | `DELETE /v1/documents/:id` | [docs](https://rotacloud.com/api/) |
| [Delete Group](actions/delete-group.md) | `DELETE /v1/groups/:id` | [docs](https://rotacloud.com/api/) |
| [Delete Leave Embargo](actions/delete-leave-embargo.md) | `DELETE /v1/leave_embargoes/:id` | [docs](https://rotacloud.com/api/) |
| [Delete Leave Entry](actions/delete-leave-entry.md) | `DELETE /v1/leave/:id` | [docs](https://rotacloud.com/api/) |
| [Delete Leave Request](actions/delete-leave-request.md) | `DELETE /v1/leave_requests/:id` | [docs](https://rotacloud.com/api/) |
| [Delete Location](actions/delete-location.md) | `DELETE /v1/locations/:id` | [docs](https://rotacloud.com/api/) |
| [Delete Logbook Category](actions/delete-logbook-category.md) | `DELETE /v2/logbook/categories/:id` | [docs](https://rotacloud.com/api/) |
| [Delete Logbook Entry](actions/delete-logbook-entry.md) | `DELETE /v2/logbook/:id` | [docs](https://rotacloud.com/api/) |
| [Delete Role](actions/delete-role.md) | `DELETE /v1/roles/:id` | [docs](https://rotacloud.com/api/) |
| [Delete Shift](actions/delete-shift.md) | `DELETE /v1/shifts/:id` | [docs](https://rotacloud.com/api/) |
| [Delete Shifts Batch](actions/delete-shifts-batch.md) | `DELETE /v1/shifts` | [docs](https://rotacloud.com/api/) |
| [Delete TOIL Accrual](actions/delete-toil-accrual.md) | `DELETE /v1/toil_accruals/:id` | [docs](https://rotacloud.com/api/) |
| [Delete User](actions/delete-user.md) | `DELETE /v1/users/:id` | [docs](https://rotacloud.com/api/) |
| [End User Break](actions/end-user-break.md) | `POST /v1/users_clocked_in/:id` | [docs](https://rotacloud.com/api/) |
| [Get Account](actions/get-account.md) | `GET /v1/accounts/:id` | [docs](https://rotacloud.com/api/) |
| [Get Attendance Record](actions/get-attendance-record.md) | `GET /v1/attendance/:id` | [docs](https://rotacloud.com/api/) |
| [Get Clocked In User](actions/get-clocked-in-user.md) | `GET /v1/users_clocked_in/:id` | [docs](https://rotacloud.com/api/) |
| [Get Day Note](actions/get-day-note.md) | `GET /v1/day_notes/:id` | [docs](https://rotacloud.com/api/) |
| [Get Day Note V2](actions/get-day-note-v2.md) | `GET /v2/dayNotes/:id` | [docs](https://rotacloud.com/api/) |
| [Get Document](actions/get-document.md) | `GET /v1/documents/:id` | [docs](https://rotacloud.com/api/) |
| [Get Group](actions/get-group.md) | `GET /v1/groups/:id` | [docs](https://rotacloud.com/api/) |
| [Get Invoice](actions/get-invoice.md) | `GET /v2/invoices/:id` | [docs](https://rotacloud.com/api/) |
| [Get Leave Embargo](actions/get-leave-embargo.md) | `GET /v1/leave_embargoes/:id` | [docs](https://rotacloud.com/api/) |
| [Get Leave Entry](actions/get-leave-entry.md) | `GET /v1/leave/:id` | [docs](https://rotacloud.com/api/) |
| [Get Leave Request](actions/get-leave-request.md) | `GET /v1/leave_requests/:id` | [docs](https://rotacloud.com/api/) |
| [Get Location](actions/get-location.md) | `GET /v1/locations/:id` | [docs](https://rotacloud.com/api/) |
| [Get Logbook Category](actions/get-logbook-category.md) | `GET /v2/logbook/categories/:id` | [docs](https://rotacloud.com/api/) |
| [Get Logbook Entry](actions/get-logbook-entry.md) | `GET /v2/logbook/:id` | [docs](https://rotacloud.com/api/) |
| [Get Pin](actions/get-pin.md) | `GET /v1/pins/:id` | [docs](https://rotacloud.com/api/) |
| [Get Role](actions/get-role.md) | `GET /v1/roles/:id` | [docs](https://rotacloud.com/api/) |
| [Get Shift](actions/get-shift.md) | `GET /v1/shifts/:id` | [docs](https://rotacloud.com/api/) |
| [Get Shift History](actions/get-shift-history.md) | `GET /v1/shifts/:id/history` | [docs](https://rotacloud.com/api/) |
| [Get Terminal](actions/get-terminal.md) | `GET /v1/terminals/:id` | [docs](https://rotacloud.com/api/) |
| [Get Timezone](actions/get-timezone.md) | `GET /v1/timezones/:id` | [docs](https://rotacloud.com/api/) |
| [Get Toil Accrual](actions/get-toil-accrual.md) | `GET /v1/toil_accruals/:id` | [docs](https://rotacloud.com/api/) |
| [Get User](actions/get-user.md) | `GET /v1/users/:id` | [docs](https://rotacloud.com/api/) |
| [Launch Active Terminal](actions/launch-active-terminal.md) | `POST /v1/terminals_active` | [docs](https://rotacloud.com/api/) |
| [List Accounts](actions/list-accounts.md) | `GET /v1/accounts` | [docs](https://rotacloud.com/api/) |
| [List Active Terminals](actions/list-active-terminals.md) | `GET /v1/terminals_active` | [docs](https://rotacloud.com/api/) |
| [List Attendance Records](actions/list-attendance-records.md) | `GET /v1/attendance` | [docs](https://rotacloud.com/api/) |
| [List Auth Context](actions/list-auth-context.md) | `GET /v1/auth` | [docs](https://rotacloud.com/api/) |
| [List Availability](actions/list-availability.md) | `GET /v1/availability` | [docs](https://rotacloud.com/api/) |
| [List Clocked In Users](actions/list-clocked-in-users.md) | `GET /v1/users_clocked_in` | [docs](https://rotacloud.com/api/) |
| [List Daily Budgets](actions/list-daily-budgets.md) | `GET /v1/daily_budgets` | [docs](https://rotacloud.com/api/) |
| [List Daily Revenue](actions/list-daily-revenue.md) | `GET /v1/daily_revenue` | [docs](https://rotacloud.com/api/) |
| [List Day Notes](actions/list-day-notes.md) | `GET /v1/day_notes` | [docs](https://rotacloud.com/api/) |
| [List Day Notes V2](actions/list-day-notes-v2.md) | `GET /v2/dayNotes` | [docs](https://rotacloud.com/api/) |
| [List Days Off](actions/list-days-off.md) | `GET /v1/days_off` | [docs](https://rotacloud.com/api/) |
| [List Documents](actions/list-documents.md) | `GET /v1/documents` | [docs](https://rotacloud.com/api/) |
| [List Groups](actions/list-groups.md) | `GET /v1/groups` | [docs](https://rotacloud.com/api/) |
| [List Invoices](actions/list-invoices.md) | `GET /v2/invoices` | [docs](https://rotacloud.com/api/) |
| [List Leave Embargoes](actions/list-leave-embargoes.md) | `GET /v1/leave_embargoes` | [docs](https://rotacloud.com/api/) |
| [List Leave Entries](actions/list-leave-entries.md) | `GET /v1/leave` | [docs](https://rotacloud.com/api/) |
| [List Leave Requests](actions/list-leave-requests.md) | `GET /v1/leave_requests` | [docs](https://rotacloud.com/api/) |
| [List Leave Types](actions/list-leave-types.md) | `GET /v1/leave_types` | [docs](https://rotacloud.com/api/) |
| [List Locations](actions/list-locations.md) | `GET /v1/locations` | [docs](https://rotacloud.com/api/) |
| [List Logbook Categories](actions/list-logbook-categories.md) | `GET /v2/logbook/categories` | [docs](https://rotacloud.com/api/) |
| [List Logbook Entries](actions/list-logbook-entries.md) | `GET /v2/logbook/user/:userId` | [docs](https://rotacloud.com/api/) |
| [List Messages](actions/list-messages.md) | `GET /v1/messages` | [docs](https://rotacloud.com/api/) |
| [List Roles](actions/list-roles.md) | `GET /v1/roles` | [docs](https://rotacloud.com/api/) |
| [List Settings](actions/list-settings.md) | `GET /v1/settings` | [docs](https://rotacloud.com/api/) |
| [List Shifts](actions/list-shifts.md) | `GET /v1/shifts` | [docs](https://rotacloud.com/api/) |
| [List Terminals](actions/list-terminals.md) | `GET /v1/terminals` | [docs](https://rotacloud.com/api/) |
| [List Timezones](actions/list-timezones.md) | `GET /v1/timezones` | [docs](https://rotacloud.com/api/) |
| [List Toil Accruals](actions/list-toil-accruals.md) | `GET /v1/toil_accruals` | [docs](https://rotacloud.com/api/) |
| [List Toil Allowance](actions/list-toil-allowance.md) | `GET /v1/toil_allowance/:year` | [docs](https://rotacloud.com/api/) |
| [List Users](actions/list-users.md) | `GET /v1/users` | [docs](https://rotacloud.com/api/) |
| [Ping Active Terminal](actions/ping-active-terminal.md) | `POST /v1/terminals_active/:id` | [docs](https://rotacloud.com/api/) |
| [Publish Shifts](actions/publish-shifts.md) | `POST /v1/shifts_published` | [docs](https://rotacloud.com/api/) |
| [Resend Onboarding Link](actions/resend-onboarding-link.md) | `POST /v2/users/onboard/:id/resend` | [docs](https://rotacloud.com/api/) |
| [Send Message](actions/send-message.md) | `POST /v1/messages` | [docs](https://rotacloud.com/api/) |
| [Start User Break](actions/start-user-break.md) | `POST /v1/users_clocked_in/:id` | [docs](https://rotacloud.com/api/) |
| [Unpublish Shifts](actions/unpublish-shifts.md) | `DELETE /v1/shifts_published` | [docs](https://rotacloud.com/api/) |
| [Update Attendance Record](actions/update-attendance-record.md) | `POST /v1/attendance/:id` | [docs](https://rotacloud.com/api/) |
| [Update Availability](actions/update-availability.md) | `POST /v1/availability` | [docs](https://rotacloud.com/api/) |
| [Update Daily Budgets Batch](actions/update-daily-budgets-batch.md) | `POST /v1/daily_budgets` | [docs](https://rotacloud.com/api/) |
| [Update Daily Revenue Batch](actions/update-daily-revenue-batch.md) | `POST /v1/daily_revenue` | [docs](https://rotacloud.com/api/) |
| [Update Day Note](actions/update-day-note.md) | `POST /v1/day_notes/:id` | [docs](https://rotacloud.com/api/) |
| [Update Day Note V2](actions/update-day-note-v2.md) | `PUT /v2/dayNotes/:id` | [docs](https://rotacloud.com/api/) |
| [Update Document](actions/update-document.md) | `POST /v1/documents/:id` | [docs](https://rotacloud.com/api/) |
| [Update Group](actions/update-group.md) | `POST /v1/groups/:id` | [docs](https://rotacloud.com/api/) |
| [Update Leave Embargo](actions/update-leave-embargo.md) | `POST /v1/leave_embargoes/:id` | [docs](https://rotacloud.com/api/) |
| [Update Leave Entry](actions/update-leave-entry.md) | `POST /v1/leave/:id` | [docs](https://rotacloud.com/api/) |
| [Update Leave Request](actions/update-leave-request.md) | `POST /v1/leave_requests/:id` | [docs](https://rotacloud.com/api/) |
| [Update Location](actions/update-location.md) | `POST /v1/locations/:id` | [docs](https://rotacloud.com/api/) |
| [Update Logbook Category](actions/update-logbook-category.md) | `PUT /v2/logbook/categories/:id` | [docs](https://rotacloud.com/api/) |
| [Update Logbook Entry](actions/update-logbook-entry.md) | `PUT /v2/logbook/:id` | [docs](https://rotacloud.com/api/) |
| [Update Role](actions/update-role.md) | `POST /v1/roles/:id` | [docs](https://rotacloud.com/api/) |
| [Update Shift](actions/update-shift.md) | `POST /v1/shifts/:id` | [docs](https://rotacloud.com/api/) |
| [Update Shift Drop Request](actions/update-shift-drop-request.md) | `POST /v1/unavailability_requests/:id/:decision` | [docs](https://rotacloud.com/api/) |
| [Update Shift Swap Request](actions/update-shift-swap-request.md) | `POST /v1/swap_requests/:id` | [docs](https://rotacloud.com/api/) |
| [Update Shifts Batch](actions/update-shifts-batch.md) | `POST /v1/shifts` | [docs](https://rotacloud.com/api/) |
| [Update Terminal](actions/update-terminal.md) | `POST /v1/terminals/:id` | [docs](https://rotacloud.com/api/) |
| [Update User](actions/update-user.md) | `POST /v1/users/:id` | [docs](https://rotacloud.com/api/) |
| [Update User Onboarding](actions/update-user-onboarding.md) | `PATCH /v2/users/onboard/:id` | [docs](https://rotacloud.com/api/) |
