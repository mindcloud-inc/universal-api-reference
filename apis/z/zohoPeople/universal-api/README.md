# <img src="https://images.mindcloud.co/apps/icons/zoho-people-1024x1024_1775229135610.png" alt="Zoho People logo" width="28" height="28"> Zoho People: Universal API

Manage employee records, leave, attendance, and HR forms

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/zohoPeople/latest
- **Category:** Human Resources / HRIS
- **Actions:** 23
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.zoho.com/people/
- **Vendor API docs:** https://www.zoho.com/people/api/overview.html

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Organization Info](actions/get-organization-info.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoPeople/latest/actions/get-organization-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (23)

### Attendance Record

| Action | Method | Description |
| --- | --- | --- |
| [Add Attendance Entries](actions/add-attendance-entries.md) | POST | Creates attendance entries in Zoho People. |
| [Add Attendance Entry by Punch In or Out](actions/add-attendance-entry-by-punch-in-or-out.md) | POST | Creates attendance entries by punch direction in Zoho People. |
| [Get Attendance Entries](actions/get-attendance-entries.md) | GET | Retrieves attendance entries from Zoho People. |
| [Get Specific Attendance Entry](actions/get-specific-attendance-entry.md) | GET | Retrieves an attendance entry from Zoho People. |

### Form

| Action | Method | Description |
| --- | --- | --- |
| [Get Form Fields](actions/get-form-fields.md) | GET | Retrieves fields for a Zoho People form. |
| [List Forms](actions/list-forms.md) | GET | Retrieves forms from Zoho People. |

### Form Record

| Action | Method | Description |
| --- | --- | --- |
| [Create Form Record](actions/create-form-record.md) | POST | Creates a record in a Zoho People form. |
| [Get Form Record](actions/get-form-record.md) | GET | Retrieves a record from a Zoho People form. |
| [Get Related Form Records](actions/get-related-form-records.md) | GET | Retrieves related records from a Zoho People form. |
| [List Form Records](actions/list-form-records.md) | GET | Retrieves records from a Zoho People form. |
| [Search Form Records](actions/search-form-records.md) | GET | Finds records in a Zoho People form. |
| [Update Form Record](actions/update-form-record.md) | PUT | Updates a record in a Zoho People form. |

### Form Record Count

| Action | Method | Description |
| --- | --- | --- |
| [Get Record Count](actions/get-record-count.md) | GET | Retrieves record count for a Zoho People form. |

### Leave Request

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Leave Request](actions/cancel-leave-request.md) | PUT | Cancels a leave request in Zoho People. |
| [Create Leave Request](actions/create-leave-request.md) | POST | Creates a leave request in Zoho People. |
| [Delete Leave Request](actions/delete-leave-request.md) | DELETE | Deletes a leave request from Zoho People. |
| [Get Leave Requests](actions/get-leave-requests.md) | GET | Retrieves leave requests from Zoho People. |
| [Get Specific Leave Request](actions/get-specific-leave-request.md) | GET | Retrieves a leave request from Zoho People. |
| [Update Leave Request](actions/update-leave-request.md) | PUT | Updates a leave request in Zoho People. |

### Organization

| Action | Method | Description |
| --- | --- | --- |
| [Get Organization Info](actions/get-organization-info.md) | GET | Retrieves organization details from Zoho People. |

### Report

| Action | Method | Description |
| --- | --- | --- |
| [Get Leave Type Summary](actions/get-leave-type-summary.md) | GET | Retrieves leave type summary from Zoho People. |

### View

| Action | Method | Description |
| --- | --- | --- |
| [List Form Views](actions/list-form-views.md) | GET | Retrieves views for a Zoho People form. |
| [List Views](actions/list-views.md) | GET | Retrieves views from Zoho People. |

