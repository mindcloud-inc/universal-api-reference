# <img src="https://images.mindcloud.co/apps/icons/h-rpartner_1775659015726.png" alt="HR Partner logo" width="28" height="28"> HR Partner: Universal API

Manage employee records, leave, recruitment, timesheets, and reviews

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/hRPartner/latest
- **Category:** Human Resources / HRIS
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.hrpartner.io
- **Vendor API docs:** https://developer.hrpartner.io

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Company](actions/get-company.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hRPartner/latest/actions/get-company?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Absence

| Action | Method | Description |
| --- | --- | --- |
| [List Absences](actions/list-absences.md) | GET |  |

### Address

| Action | Method | Description |
| --- | --- | --- |
| [List Employee Addresses](actions/list-employee-addresses.md) | GET |  |

### Applicant

| Action | Method | Description |
| --- | --- | --- |
| [Add or Update Applicant](actions/add-or-update-applicant.md) | PUT |  |
| [Get Applicant](actions/get-applicant.md) | GET |  |
| [List Applicants](actions/list-applicants.md) | GET |  |

### Application

| Action | Method | Description |
| --- | --- | --- |
| [Add or Update Application](actions/add-or-update-application.md) | PUT |  |
| [Get Application](actions/get-application.md) | GET |  |
| [List Applications](actions/list-applications.md) | GET |  |

### Application Stage

| Action | Method | Description |
| --- | --- | --- |
| [Get Application Stage Tracking](actions/get-application-stage-tracking.md) | GET |  |

### Asset

| Action | Method | Description |
| --- | --- | --- |
| [List Assets](actions/list-assets.md) | GET |  |

### Benefit

| Action | Method | Description |
| --- | --- | --- |
| [List Benefits](actions/list-benefits.md) | GET |  |

### Checklist

| Action | Method | Description |
| --- | --- | --- |
| [List Checklists](actions/list-checklists.md) | GET |  |

### Company

| Action | Method | Description |
| --- | --- | --- |
| [Get Company](actions/get-company.md) | GET |  |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [List Employee Contacts](actions/list-employee-contacts.md) | GET |  |

### Dependent

| Action | Method | Description |
| --- | --- | --- |
| [List Dependents](actions/list-dependents.md) | GET |  |

### Education

| Action | Method | Description |
| --- | --- | --- |
| [List Education Records](actions/list-education-records.md) | GET |  |

### Employee

| Action | Method | Description |
| --- | --- | --- |
| [Add or Update Employee](actions/add-or-update-employee.md) | PUT |  |
| [Get Employee](actions/get-employee.md) | GET |  |
| [List Employees](actions/list-employees.md) | GET |  |

### Expense Claim

| Action | Method | Description |
| --- | --- | --- |
| [List Expense Claims](actions/list-expense-claims.md) | GET |  |

### Goal

| Action | Method | Description |
| --- | --- | --- |
| [List Goals](actions/list-goals.md) | GET |  |

### Job

| Action | Method | Description |
| --- | --- | --- |
| [Get Job Listing](actions/get-job-listing.md) | GET |  |
| [List Job Listings](actions/list-job-listings.md) | GET |  |

### Leave Balance

| Action | Method | Description |
| --- | --- | --- |
| [List Leave Balances](actions/list-leave-balances.md) | GET |  |

### Leave Request

| Action | Method | Description |
| --- | --- | --- |
| [Get Leave Request](actions/get-leave-request.md) | GET |  |
| [List Leave Requests](actions/list-leave-requests.md) | GET |  |

### Library Category

| Action | Method | Description |
| --- | --- | --- |
| [List Library Categories](actions/list-library-categories.md) | GET |  |

### Library Document

| Action | Method | Description |
| --- | --- | --- |
| [List Library Documents](actions/list-library-documents.md) | GET |  |

### Note

| Action | Method | Description |
| --- | --- | --- |
| [List Notes](actions/list-notes.md) | GET |  |

### Performance Review

| Action | Method | Description |
| --- | --- | --- |
| [List Performance Reviews](actions/list-performance-reviews.md) | GET |  |

### Position

| Action | Method | Description |
| --- | --- | --- |
| [List Positions](actions/list-positions.md) | GET |  |

### Reminder

| Action | Method | Description |
| --- | --- | --- |
| [Get Reminder](actions/get-reminder.md) | GET |  |
| [List Reminders](actions/list-reminders.md) | GET |  |
| [Update Reminder](actions/update-reminder.md) | PUT |  |

### Review

| Action | Method | Description |
| --- | --- | --- |
| [List Reviews](actions/list-reviews.md) | GET |  |

### Skill

| Action | Method | Description |
| --- | --- | --- |
| [List Skills](actions/list-skills.md) | GET |  |

### Timeclock Entry

| Action | Method | Description |
| --- | --- | --- |
| [Add Timeclock Entry](actions/add-timeclock-entry.md) | POST |  |

### Timesheet

| Action | Method | Description |
| --- | --- | --- |
| [Get Timesheet](actions/get-timesheet.md) | GET |  |
| [List Timesheets](actions/list-timesheets.md) | GET |  |

### Training

| Action | Method | Description |
| --- | --- | --- |
| [List Training Records](actions/list-training-records.md) | GET |  |

