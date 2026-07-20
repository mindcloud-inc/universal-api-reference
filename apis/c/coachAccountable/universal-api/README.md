# <img src="https://images.mindcloud.co/apps/icons/coach-accountable_1774032154246.png" alt="CoachAccountable logo" width="28" height="28"> CoachAccountable: Universal API

CoachAccountable API wrapper for client, action, metric, appointment, session, agreement, invoice, engagement, course, and group workflows.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/coachAccountable/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 99
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.coachaccountable.com
- **Vendor API docs:** https://www.coachaccountable.com/APIDocs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Account Profile](actions/get-account-profile.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/coachAccountable/latest/actions/get-account-profile?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (99)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Get Account Profile](actions/get-account-profile.md) | GET | Retrieves an account profile from CoachAccountable. |

### Action

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Action](actions/cancel-action.md) | PUT | Cancels an action in CoachAccountable. |
| [Create Action](actions/create-action.md) | POST | Creates an action in CoachAccountable. |
| [Delete Action](actions/delete-action.md) | DELETE | Deletes an action from CoachAccountable. |
| [List Actions](actions/list-actions.md) | GET | Retrieves actions from CoachAccountable. |
| [Mark Action Done](actions/mark-action-done.md) | PUT | Marks an action done in CoachAccountable. |
| [Uncancel Action](actions/uncancel-action.md) | PUT | Uncancels an action in CoachAccountable. |
| [Unmark Action Done](actions/unmark-action-done.md) | PUT | Unmarks an action done in CoachAccountable. |
| [Update Action](actions/update-action.md) | PUT | Updates an action in CoachAccountable. |

### Action Project

| Action | Method | Description |
| --- | --- | --- |
| [Delete Action Project](actions/delete-action-project.md) | DELETE | Deletes an action project from CoachAccountable. |
| [List Action Projects](actions/list-action-projects.md) | GET | Retrieves action projects from CoachAccountable. |

### Action Reminder

| Action | Method | Description |
| --- | --- | --- |
| [Clear Action Reminders](actions/clear-action-reminders.md) | PUT | Clears action reminders in CoachAccountable. |
| [Delete Action Reminder](actions/delete-action-reminder.md) | DELETE | Deletes an action reminder from CoachAccountable. |
| [List Action Reminders](actions/list-action-reminders.md) | GET | Retrieves action reminders from CoachAccountable. |
| [Set Action Reminders](actions/set-action-reminders.md) | PUT | Updates action reminders in CoachAccountable. |

### Agreement

| Action | Method | Description |
| --- | --- | --- |
| [Delete Agreement](actions/delete-agreement.md) | DELETE | Deletes an agreement from CoachAccountable. |
| [Issue Agreement](actions/issue-agreement.md) | POST | Issues an agreement in CoachAccountable. |
| [List Agreements](actions/list-agreements.md) | GET | Retrieves agreements from CoachAccountable. |

### Agreement Template

| Action | Method | Description |
| --- | --- | --- |
| [List Agreement Templates](actions/list-agreement-templates.md) | GET | Retrieves agreement templates from CoachAccountable. |

### Appointment

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Appointment](actions/cancel-appointment.md) | PUT | Cancels an appointment in CoachAccountable. |
| [Create Appointment](actions/create-appointment.md) | POST | Creates an appointment in CoachAccountable. |
| [Delete Appointment](actions/delete-appointment.md) | DELETE | Deletes an appointment from CoachAccountable. |
| [List Appointments](actions/list-appointments.md) | GET | Retrieves appointments from CoachAccountable. |

### Appointment Setting

| Action | Method | Description |
| --- | --- | --- |
| [Get Client Appointment Settings](actions/get-client-appointment-settings.md) | GET | Retrieves client appointment settings from CoachAccountable. |
| [Set Client Appointment Settings](actions/set-client-appointment-settings.md) | PUT | Updates client appointment settings in CoachAccountable. |

### Appointment Type

| Action | Method | Description |
| --- | --- | --- |
| [List Appointment Types](actions/list-appointment-types.md) | GET | Retrieves appointment types from CoachAccountable. |

### Client

| Action | Method | Description |
| --- | --- | --- |
| [Activate Client](actions/activate-client.md) | PUT | Activates a client in CoachAccountable. |
| [Create Client](actions/create-client.md) | POST | Creates a client in CoachAccountable. |
| [Deactivate Client](actions/deactivate-client.md) | PUT | Deactivates a client in CoachAccountable. |
| [Delete Client](actions/delete-client.md) | DELETE | Deletes a client from CoachAccountable. |
| [Get Client](actions/get-client.md) | GET | Retrieves a client from CoachAccountable. |
| [Invite Client](actions/invite-client.md) | POST | Sends a client invite in CoachAccountable. |
| [List Clients](actions/list-clients.md) | GET | Retrieves clients from CoachAccountable. |
| [Update Client](actions/update-client.md) | PUT | Updates a client in CoachAccountable. |

### Client Data

| Action | Method | Description |
| --- | --- | --- |
| [Get Client Data By Field](actions/get-client-data-by-field.md) | GET | Retrieves client data by field from CoachAccountable. |

### Client Data Activity Stats

| Action | Method | Description |
| --- | --- | --- |
| [Get Client Data Activity Stats](actions/get-client-data-activity-stats.md) | GET | Retrieves client activity stats from CoachAccountable. |

### Client File

| Action | Method | Description |
| --- | --- | --- |
| [Add Client File From URL](actions/add-client-file-from-url.md) | POST | Adds a client file from a URL in CoachAccountable. |
| [Upload Client File](actions/upload-client-file.md) | POST | Uploads a client file to CoachAccountable. |

### Client Profile

| Action | Method | Description |
| --- | --- | --- |
| [Set Client Profile Extra](actions/set-client-profile-extra.md) | PUT | Updates client profile extras in CoachAccountable. |

### Company

| Action | Method | Description |
| --- | --- | --- |
| [List Companies](actions/list-companies.md) | GET | Retrieves companies from CoachAccountable. |

### Course

| Action | Method | Description |
| --- | --- | --- |
| [List Courses](actions/list-courses.md) | GET | Retrieves courses from CoachAccountable. |

### Course Availability

| Action | Method | Description |
| --- | --- | --- |
| [Add Course Client Availability](actions/add-course-client-availability.md) | POST | Adds course client availability in CoachAccountable. |
| [List Course Availabilities](actions/list-course-availabilities.md) | GET | Retrieves course availabilities from CoachAccountable. |
| [List Course Client Availabilities](actions/list-course-client-availabilities.md) | GET | Retrieves course client availabilities from CoachAccountable. |
| [Remove Course Client Availability](actions/remove-course-client-availability.md) | DELETE | Removes course client availability from CoachAccountable. |

### Course Enrollment

| Action | Method | Description |
| --- | --- | --- |
| [Enroll Client in Course](actions/enroll-client-in-course.md) | POST | Enrolls a client in a CoachAccountable course. |

### Course Participant

| Action | Method | Description |
| --- | --- | --- |
| [Fast Forward Course Participant](actions/fast-forward-course-participant.md) | PUT | Fast-forwards a course participant in CoachAccountable. |
| [List Course Client Participants](actions/list-course-client-participants.md) | GET | Retrieves course client participants from CoachAccountable. |
| [List Course Group Participants](actions/list-course-group-participants.md) | GET | Retrieves course group participants from CoachAccountable. |
| [Pause Course Participant](actions/pause-course-participant.md) | PUT | Pauses a course participant in CoachAccountable. |
| [Rewind Course Participant](actions/rewind-course-participant.md) | PUT | Rewinds a course participant in CoachAccountable. |
| [Stop Course Participant](actions/stop-course-participant.md) | PUT | Stops a course participant in CoachAccountable. |
| [Unpause Course Participant](actions/unpause-course-participant.md) | PUT | Unpauses a course participant in CoachAccountable. |

### Engagement

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Engagement](actions/cancel-engagement.md) | PUT | Cancels an engagement in CoachAccountable. |
| [Complete Engagement](actions/complete-engagement.md) | PUT | Completes an engagement in CoachAccountable. |
| [Create Engagement for Client](actions/create-engagement-for-client.md) | POST | Creates a client engagement in CoachAccountable. |
| [Delete Engagement](actions/delete-engagement.md) | DELETE | Deletes an engagement from CoachAccountable. |
| [List Engagements](actions/list-engagements.md) | GET | Retrieves engagements from CoachAccountable. |
| [Reopen Engagement](actions/reopen-engagement.md) | PUT | Reopens an engagement in CoachAccountable. |
| [Update Engagement](actions/update-engagement.md) | PUT | Updates an engagement in CoachAccountable. |

### Engagement Template

| Action | Method | Description |
| --- | --- | --- |
| [List Engagement Templates](actions/list-engagement-templates.md) | GET | Retrieves engagement templates from CoachAccountable. |

### Group

| Action | Method | Description |
| --- | --- | --- |
| [List Groups](actions/list-groups.md) | GET | Retrieves groups from CoachAccountable. |

### Group Member

| Action | Method | Description |
| --- | --- | --- |
| [Activate Group Client Member](actions/activate-group-client-member.md) | PUT | Activates a group client member in CoachAccountable. |
| [Add Client to Group](actions/add-client-to-group.md) | POST | Adds a client to a CoachAccountable group. |
| [Deactivate Group Client Member](actions/deactivate-group-client-member.md) | PUT | Deactivates a group client member in CoachAccountable. |
| [List Group Client Members](actions/list-group-client-members.md) | GET | Retrieves group client members from CoachAccountable. |
| [List Group Coach Members](actions/list-group-coach-members.md) | GET | Retrieves group coach members from CoachAccountable. |
| [Remove Group Client Member](actions/remove-group-client-member.md) | DELETE | Removes a group client member from CoachAccountable. |

### Invoice

| Action | Method | Description |
| --- | --- | --- |
| [Create Invoice](actions/create-invoice.md) | POST | Creates an invoice in CoachAccountable. |
| [Delete Invoice](actions/delete-invoice.md) | DELETE | Deletes an invoice from CoachAccountable. |
| [Get Invoice](actions/get-invoice.md) | GET | Retrieves an invoice from CoachAccountable. |
| [List Invoices](actions/list-invoices.md) | GET | Retrieves invoices from CoachAccountable. |
| [Send Invoice](actions/send-invoice.md) | PUT | Sends an invoice from CoachAccountable. |
| [Update Invoice](actions/update-invoice.md) | PUT | Updates an invoice in CoachAccountable. |

### Invoice Payment

| Action | Method | Description |
| --- | --- | --- |
| [Delete Invoice Payment](actions/delete-invoice-payment.md) | DELETE | Deletes an invoice payment from CoachAccountable. |
| [List Invoice Payments](actions/list-invoice-payments.md) | GET | Retrieves invoice payments from CoachAccountable. |
| [Record Invoice Payment](actions/record-invoice-payment.md) | POST | Records an invoice payment in CoachAccountable. |

### Metric

| Action | Method | Description |
| --- | --- | --- |
| [Create Metric](actions/create-metric.md) | POST | Creates a metric in CoachAccountable. |
| [Delete Metric](actions/delete-metric.md) | DELETE | Deletes a metric from CoachAccountable. |
| [List Metrics](actions/list-metrics.md) | GET | Retrieves metrics from CoachAccountable. |
| [Mark Metric Complete](actions/mark-metric-complete.md) | PUT | Marks a metric complete in CoachAccountable. |
| [Unmark Metric Complete](actions/unmark-metric-complete.md) | PUT | Unmarks a metric complete in CoachAccountable. |
| [Update Metric](actions/update-metric.md) | PUT | Updates a metric in CoachAccountable. |

### Metric Data

| Action | Method | Description |
| --- | --- | --- |
| [Add Metric Data](actions/add-metric-data.md) | POST | Adds metric data in CoachAccountable. |
| [Clear Metric Day Data](actions/clear-metric-day-data.md) | PUT | Clears metric day data in CoachAccountable. |

### Offering

| Action | Method | Description |
| --- | --- | --- |
| [List Offerings](actions/list-offerings.md) | GET | Retrieves offerings from CoachAccountable. |

### Offering Collection

| Action | Method | Description |
| --- | --- | --- |
| [List Offering Collections](actions/list-offering-collections.md) | GET | Retrieves offering collections from CoachAccountable. |

### Offering Submission

| Action | Method | Description |
| --- | --- | --- |
| [List Offering Submissions](actions/list-offering-submissions.md) | GET | Retrieves offering submissions from CoachAccountable. |

### Personnel

| Action | Method | Description |
| --- | --- | --- |
| [List Personnel](actions/list-personnel.md) | GET | Retrieves personnel from CoachAccountable. |

### Session

| Action | Method | Description |
| --- | --- | --- |
| [Create Session](actions/create-session.md) | POST | Creates a session in CoachAccountable. |
| [Delete Session](actions/delete-session.md) | DELETE | Deletes a session from CoachAccountable. |
| [List Sessions](actions/list-sessions.md) | GET | Retrieves sessions from CoachAccountable. |
| [Update Session](actions/update-session.md) | PUT | Updates a session in CoachAccountable. |

### Worksheet

| Action | Method | Description |
| --- | --- | --- |
| [Delete Worksheet](actions/delete-worksheet.md) | DELETE | Deletes a worksheet from CoachAccountable. |
| [List Worksheets](actions/list-worksheets.md) | GET | Retrieves worksheets from CoachAccountable. |

### Worksheet Reminder

| Action | Method | Description |
| --- | --- | --- |
| [Clear Worksheet Reminders](actions/clear-worksheet-reminders.md) | PUT | Clears worksheet reminders in CoachAccountable. |
| [Delete Worksheet Reminder](actions/delete-worksheet-reminder.md) | DELETE | Deletes a worksheet reminder from CoachAccountable. |
| [List Worksheet Reminders](actions/list-worksheet-reminders.md) | GET | Retrieves worksheet reminders from CoachAccountable. |
| [Set Worksheet Reminders](actions/set-worksheet-reminders.md) | PUT | Updates worksheet reminders in CoachAccountable. |

