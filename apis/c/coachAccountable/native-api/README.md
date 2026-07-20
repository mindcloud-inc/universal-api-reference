# CoachAccountable: Native API Reference

A consolidated summary of CoachAccountable's API configuration and 99 documented operations, with links to official documentation.

- **Official docs:** https://www.coachaccountable.com/APIDocs
- **API base URL:** `https://www.coachaccountable.com/API`

## Authentication

### API Key

Connect CoachAccountable using your API ID plus private API key from the official API docs page.

### Credentials

- **API Key:** `apiKey` · required
- **API ID:** `apiId` · required · Your CoachAccountable API ID. In the official API docs, open any "try this..." form while signed in and copy the prefilled APIID value.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://www.coachaccountable.com/APIDocs)

## API conventions

Request bodies use URL-encoded form data.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/x-www-form-urlencoded` |

Response data is read from `return`.

## Endpoints (99 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Activate Client](actions/activate-client.md) | `POST /` | [docs](https://www.coachaccountable.com/APIDocs#Client.activate) |
| [Activate Group Client Member](actions/activate-group-client-member.md) | `POST /` | [docs](https://www.coachaccountable.com/APIDocs#Group.activateClientMember) |
| [Add Client File From URL](actions/add-client-file-from-url.md) | `POST /` | [docs](https://www.coachaccountable.com/APIDocs#ClientFile.addAsURL) |
| [Add Client to Group](actions/add-client-to-group.md) | `POST /` | [docs](https://www.coachaccountable.com/APIDocs#Group.addClientMember) |
| [Add Course Client Availability](actions/add-course-client-availability.md) | `POST /` | [docs](https://www.coachaccountable.com/APIDocs#Course.addClientAvailability) |
| [Add Metric Data](actions/add-metric-data.md) | `POST /` | [docs](https://www.coachaccountable.com/APIDocs#Metric.addData) |
| [Cancel Action](actions/cancel-action.md) | `POST /` | [docs](https://www.coachaccountable.com/APIDocs#Action.cancel) |
| [Cancel Appointment](actions/cancel-appointment.md) | `POST /` | [docs](https://www.coachaccountable.com/APIDocs#Appointment.cancel) |
| [Cancel Engagement](actions/cancel-engagement.md) | `POST /` | [docs](https://www.coachaccountable.com/APIDocs#Engagement.cancel) |
| [Clear Action Reminders](actions/clear-action-reminders.md) | `POST /` | [docs](https://www.coachaccountable.com/APIDocs#Action.clearReminders) |
| [Clear Metric Day Data](actions/clear-metric-day-data.md) | `POST /` | [docs](https://www.coachaccountable.com/APIDocs#Metric.clearDayData) |
| [Clear Worksheet Reminders](actions/clear-worksheet-reminders.md) | `POST /` | [docs](https://www.coachaccountable.com/APIDocs#Worksheet.clearReminders) |
| [Complete Engagement](actions/complete-engagement.md) | `POST /` | [docs](https://www.coachaccountable.com/APIDocs#Engagement.complete) |
| [Create Action](actions/create-action.md) | `POST /` | [docs](https://www.coachaccountable.com/APIDocs#Action.add) |
| [Create Appointment](actions/create-appointment.md) | `POST /` | [docs](https://www.coachaccountable.com/APIDocs#Appointment.add) |
| [Create Client](actions/create-client.md) | `POST /` | [docs](https://www.coachaccountable.com/APIDocs#Client.add) |
| [Create Engagement for Client](actions/create-engagement-for-client.md) | `POST /` | [docs](https://www.coachaccountable.com/APIDocs#Engagement.addForClient) |
| [Create Invoice](actions/create-invoice.md) | `POST /` | [docs](https://www.coachaccountable.com/APIDocs#Invoice.add) |
| [Create Metric](actions/create-metric.md) | `POST /` | [docs](https://www.coachaccountable.com/APIDocs#Metric.add) |
| [Create Session](actions/create-session.md) | `POST /` | [docs](https://www.coachaccountable.com/APIDocs#Session.add) |
| [Deactivate Client](actions/deactivate-client.md) | `POST /` | [docs](https://www.coachaccountable.com/APIDocs#Client.deactivate) |
| [Deactivate Group Client Member](actions/deactivate-group-client-member.md) | `POST /` | [docs](https://www.coachaccountable.com/APIDocs#Group.deactivateClientMember) |
| [Delete Action](actions/delete-action.md) | `POST /` | [docs](https://www.coachaccountable.com/APIDocs#Action.delete) |
| [Delete Action Project](actions/delete-action-project.md) | `POST /` | [docs](https://www.coachaccountable.com/APIDocs#Action.deleteProject) |
| [Delete Action Reminder](actions/delete-action-reminder.md) | `POST /` | [docs](https://www.coachaccountable.com/APIDocs#Action.deleteReminder) |
| [Delete Agreement](actions/delete-agreement.md) | `POST /` | [docs](https://www.coachaccountable.com/APIDocs#Agreement.delete) |
| [Delete Appointment](actions/delete-appointment.md) | `POST /` | [docs](https://www.coachaccountable.com/APIDocs#Appointment.delete) |
| [Delete Client](actions/delete-client.md) | `POST /` | [docs](https://www.coachaccountable.com/APIDocs#Client.delete) |
| [Delete Engagement](actions/delete-engagement.md) | `POST /` | [docs](https://www.coachaccountable.com/APIDocs#Engagement.delete) |
| [Delete Invoice](actions/delete-invoice.md) | `POST /` | [docs](https://www.coachaccountable.com/APIDocs#Invoice.delete) |
| [Delete Invoice Payment](actions/delete-invoice-payment.md) | `POST /` | [docs](https://www.coachaccountable.com/APIDocs#Invoice.deletePayment) |
| [Delete Metric](actions/delete-metric.md) | `POST /` | [docs](https://www.coachaccountable.com/APIDocs#Metric.delete) |
| [Delete Session](actions/delete-session.md) | `POST /` | [docs](https://www.coachaccountable.com/APIDocs#Session.delete) |
| [Delete Worksheet](actions/delete-worksheet.md) | `POST /` | [docs](https://www.coachaccountable.com/APIDocs#Worksheet.delete) |
| [Delete Worksheet Reminder](actions/delete-worksheet-reminder.md) | `POST /` | [docs](https://www.coachaccountable.com/APIDocs#Worksheet.deleteReminder) |
| [Enroll Client in Course](actions/enroll-client-in-course.md) | `POST /` | [docs](https://www.coachaccountable.com/APIDocs#Course.addClientParticipant) |
| [Fast Forward Course Participant](actions/fast-forward-course-participant.md) | `POST /` | [docs](https://www.coachaccountable.com/APIDocs#Course.fastForwardParticipant) |
| [Get Account Profile](actions/get-account-profile.md) | `POST /` | [docs](https://www.coachaccountable.com/APIDocs#Account.me) |
| [Get Client](actions/get-client.md) | `POST /` | [docs](https://www.coachaccountable.com/APIDocs#Client.get) |
| [Get Client Appointment Settings](actions/get-client-appointment-settings.md) | `POST /` | [docs](https://www.coachaccountable.com/APIDocs#Client.getAppointmentSettings) |
| [Get Client Data Activity Stats](actions/get-client-data-activity-stats.md) | `POST /` | [docs](https://www.coachaccountable.com/APIDocs#ClientData.getActivityStats) |
| [Get Client Data By Field](actions/get-client-data-by-field.md) | `POST /` | [docs](https://www.coachaccountable.com/APIDocs#ClientData.getByField) |
| [Get Invoice](actions/get-invoice.md) | `POST /` | [docs](https://www.coachaccountable.com/APIDocs#Invoice.get) |
| [Invite Client](actions/invite-client.md) | `POST /` | [docs](https://www.coachaccountable.com/APIDocs#Client.invite) |
| [Issue Agreement](actions/issue-agreement.md) | `POST /` | [docs](https://www.coachaccountable.com/APIDocs#Agreement.issue) |
| [List Action Projects](actions/list-action-projects.md) | `POST /` | [docs](https://www.coachaccountable.com/APIDocs#Action.getAllProjects) |
| [List Action Reminders](actions/list-action-reminders.md) | `POST /` | [docs](https://www.coachaccountable.com/APIDocs#Action.getReminders) |
| [List Actions](actions/list-actions.md) | `POST /` | [docs](https://www.coachaccountable.com/APIDocs#Action.getAll) |
| [List Agreement Templates](actions/list-agreement-templates.md) | `POST /` | [docs](https://www.coachaccountable.com/APIDocs#Agreement.getTemplates) |
| [List Agreements](actions/list-agreements.md) | `POST /` | [docs](https://www.coachaccountable.com/APIDocs#Agreement.getAll) |
| [List Appointment Types](actions/list-appointment-types.md) | `POST /` | [docs](https://www.coachaccountable.com/APIDocs#Appointment.getTypes) |
| [List Appointments](actions/list-appointments.md) | `POST /` | [docs](https://www.coachaccountable.com/APIDocs#Appointment.getAll) |
| [List Clients](actions/list-clients.md) | `POST /` | [docs](https://www.coachaccountable.com/APIDocs#Client.getAll) |
| [List Companies](actions/list-companies.md) | `POST /` | [docs](https://www.coachaccountable.com/APIDocs#Company.getAll) |
| [List Course Availabilities](actions/list-course-availabilities.md) | `POST /` | [docs](https://www.coachaccountable.com/APIDocs#Course.getAvailabilitiesForCourse) |
| [List Course Client Availabilities](actions/list-course-client-availabilities.md) | `POST /` | [docs](https://www.coachaccountable.com/APIDocs#Course.getAvailabilitiesForClient) |
| [List Course Client Participants](actions/list-course-client-participants.md) | `POST /` | [docs](https://www.coachaccountable.com/APIDocs#Course.getAllClientParticipants) |
| [List Course Group Participants](actions/list-course-group-participants.md) | `POST /` | [docs](https://www.coachaccountable.com/APIDocs#Course.getAllGroupParticipants) |
| [List Courses](actions/list-courses.md) | `POST /` | [docs](https://www.coachaccountable.com/APIDocs#Course.getAll) |
| [List Engagement Templates](actions/list-engagement-templates.md) | `POST /` | [docs](https://www.coachaccountable.com/APIDocs#Engagement.getTemplates) |
| [List Engagements](actions/list-engagements.md) | `POST /` | [docs](https://www.coachaccountable.com/APIDocs#Engagement.getAll) |
| [List Group Client Members](actions/list-group-client-members.md) | `POST /` | [docs](https://www.coachaccountable.com/APIDocs#Group.getAllClientMembers) |
| [List Group Coach Members](actions/list-group-coach-members.md) | `POST /` | [docs](https://www.coachaccountable.com/APIDocs#Group.getAllCoachMembers) |
| [List Groups](actions/list-groups.md) | `POST /` | [docs](https://www.coachaccountable.com/APIDocs#Group.getAll) |
| [List Invoice Payments](actions/list-invoice-payments.md) | `POST /` | [docs](https://www.coachaccountable.com/APIDocs#Invoice.getPayments) |
| [List Invoices](actions/list-invoices.md) | `POST /` | [docs](https://www.coachaccountable.com/APIDocs#Invoice.getAll) |
| [List Metrics](actions/list-metrics.md) | `POST /` | [docs](https://www.coachaccountable.com/APIDocs#Metric.getAll) |
| [List Offering Collections](actions/list-offering-collections.md) | `POST /` | [docs](https://www.coachaccountable.com/APIDocs#OfferingCollection.getAll) |
| [List Offering Submissions](actions/list-offering-submissions.md) | `POST /` | [docs](https://www.coachaccountable.com/APIDocs#Offering.getSubmissions) |
| [List Offerings](actions/list-offerings.md) | `POST /` | [docs](https://www.coachaccountable.com/APIDocs#Offering.getAll) |
| [List Personnel](actions/list-personnel.md) | `POST /` | [docs](https://www.coachaccountable.com/APIDocs#Personnel.getAll) |
| [List Sessions](actions/list-sessions.md) | `POST /` | [docs](https://www.coachaccountable.com/APIDocs#Session.getAll) |
| [List Worksheet Reminders](actions/list-worksheet-reminders.md) | `POST /` | [docs](https://www.coachaccountable.com/APIDocs#Worksheet.getReminders) |
| [List Worksheets](actions/list-worksheets.md) | `POST /` | [docs](https://www.coachaccountable.com/APIDocs#Worksheet.getAll) |
| [Mark Action Done](actions/mark-action-done.md) | `POST /` | [docs](https://www.coachaccountable.com/APIDocs#Action.markDone) |
| [Mark Metric Complete](actions/mark-metric-complete.md) | `POST /` | [docs](https://www.coachaccountable.com/APIDocs#Metric.markComplete) |
| [Pause Course Participant](actions/pause-course-participant.md) | `POST /` | [docs](https://www.coachaccountable.com/APIDocs#Course.pauseParticipant) |
| [Record Invoice Payment](actions/record-invoice-payment.md) | `POST /` | [docs](https://www.coachaccountable.com/APIDocs#Invoice.addPayment) |
| [Remove Course Client Availability](actions/remove-course-client-availability.md) | `POST /` | [docs](https://www.coachaccountable.com/APIDocs#Course.removeClientAvailability) |
| [Remove Group Client Member](actions/remove-group-client-member.md) | `POST /` | [docs](https://www.coachaccountable.com/APIDocs#Group.removeClientMember) |
| [Reopen Engagement](actions/reopen-engagement.md) | `POST /` | [docs](https://www.coachaccountable.com/APIDocs#Engagement.reopen) |
| [Rewind Course Participant](actions/rewind-course-participant.md) | `POST /` | [docs](https://www.coachaccountable.com/APIDocs#Course.rewindParticipant) |
| [Send Invoice](actions/send-invoice.md) | `POST /` | [docs](https://www.coachaccountable.com/APIDocs#Invoice.send) |
| [Set Action Reminders](actions/set-action-reminders.md) | `POST /` | [docs](https://www.coachaccountable.com/APIDocs#Action.setReminders) |
| [Set Client Appointment Settings](actions/set-client-appointment-settings.md) | `POST /` | [docs](https://www.coachaccountable.com/APIDocs#Client.setAppointmentSettings) |
| [Set Client Profile Extra](actions/set-client-profile-extra.md) | `POST /` | [docs](https://www.coachaccountable.com/APIDocs#Client.setProfileExtra) |
| [Set Worksheet Reminders](actions/set-worksheet-reminders.md) | `POST /` | [docs](https://www.coachaccountable.com/APIDocs#Worksheet.setReminders) |
| [Stop Course Participant](actions/stop-course-participant.md) | `POST /` | [docs](https://www.coachaccountable.com/APIDocs#Course.stopParticipant) |
| [Uncancel Action](actions/uncancel-action.md) | `POST /` | [docs](https://www.coachaccountable.com/APIDocs#Action.uncancel) |
| [Unmark Action Done](actions/unmark-action-done.md) | `POST /` | [docs](https://www.coachaccountable.com/APIDocs#Action.unmarkDone) |
| [Unmark Metric Complete](actions/unmark-metric-complete.md) | `POST /` | [docs](https://www.coachaccountable.com/APIDocs#Metric.unmarkComplete) |
| [Unpause Course Participant](actions/unpause-course-participant.md) | `POST /` | [docs](https://www.coachaccountable.com/APIDocs#Course.unpauseParticipant) |
| [Update Action](actions/update-action.md) | `POST /` | [docs](https://www.coachaccountable.com/APIDocs#Action.update) |
| [Update Client](actions/update-client.md) | `POST /` | [docs](https://www.coachaccountable.com/APIDocs#Client.update) |
| [Update Engagement](actions/update-engagement.md) | `POST /` | [docs](https://www.coachaccountable.com/APIDocs#Engagement.update) |
| [Update Invoice](actions/update-invoice.md) | `POST /` | [docs](https://www.coachaccountable.com/APIDocs#Invoice.update) |
| [Update Metric](actions/update-metric.md) | `POST /` | [docs](https://www.coachaccountable.com/APIDocs#Metric.update) |
| [Update Session](actions/update-session.md) | `POST /` | [docs](https://www.coachaccountable.com/APIDocs#Session.update) |
| [Upload Client File](actions/upload-client-file.md) | `POST /` | [docs](https://www.coachaccountable.com/APIDocs#ClientFile.addAsUpload) |
