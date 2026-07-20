# Zoho People: Native API Reference

A consolidated summary of Zoho People's API configuration and 23 documented operations, with links to official documentation.

- **Official docs:** https://www.zoho.com/people/api/overview.html
- **API base URL:** `https://people.zoho.com`

## Authentication

### OAuth 2

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://accounts.zoho.com/oauth/v2/auth to approve access.
2. Exchange the returned authorization code with a POST request to {{credentials.authorizeRequest.["accounts-server"]}}/oauth/v2/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `ZOHOPEOPLE.organization.READ ZOHOPEOPLE.forms.READ ZOHOPEOPLE.forms.CREATE ZOHOPEOPLE.forms.UPDATE ZOHOPEOPLE.leave.READ ZOHOPEOPLE.leave.CREATE ZOHOPEOPLE.leave.UPDATE ZOHOPEOPLE.leave.DELETE ZOHOPEOPLE.attendance.READ ZOHOPEOPLE.attendance.CREATE ZOHOPEOPLE.attendance.UPDATE`.

The flow supports refresh tokens. Refresh expired access tokens with a POST request to {{credentials.authorizeRequest.["accounts-server"]}}/oauth/v2/token.

[Official authentication documentation](https://www.zoho.com/people/api/oauth.html)

## API conventions

Responses from this API use JSON.

## Endpoints (23 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Attendance Entries](actions/add-attendance-entries.md) | `POST /api/v3/attendance/entries` | [docs](https://www.zoho.com/people/api/v3/attendance/entries-bulk-add.html) |
| [Add Attendance Entry by Punch In or Out](actions/add-attendance-entry-by-punch-in-or-out.md) | `POST /api/v3/attendance/entries/:direction` | [docs](https://www.zoho.com/people/api/v3/attendance/entries-punch-in-or-out.html) |
| [Cancel Leave Request](actions/cancel-leave-request.md) | `PATCH /api/v3/leave-tracker/leaves/:recordId` | [docs](https://www.zoho.com/people/api/v3/leave-tracker/cancel-leave.html) |
| [Create Form Record](actions/create-form-record.md) | `POST /api/forms/json/:formLinkName/insertRecord` | [docs](https://www.zoho.com/people/api/insert-records.html) |
| [Create Leave Request](actions/create-leave-request.md) | `POST /api/v3/leave-tracker/leaves` | [docs](https://www.zoho.com/people/api/v3/leave-tracker/add-leave.html) |
| [Delete Leave Request](actions/delete-leave-request.md) | `DELETE /api/v3/leave-tracker/leaves/:recordId` | [docs](https://www.zoho.com/people/api/v3/leave-tracker/delete-leave.html) |
| [Get Attendance Entries](actions/get-attendance-entries.md) | `GET /api/v3/attendance/entries` | [docs](https://www.zoho.com/people/api/v3/attendance/entries.html) |
| [Get Form Fields](actions/get-form-fields.md) | `GET /api/forms/:formLinkName/components` | [docs](https://www.zoho.com/people/api/forms-api/get-field-forms.html) |
| [Get Form Record](actions/get-form-record.md) | `GET /api/forms/:formLinkName/getDataByID` | [docs](https://www.zoho.com/people/api/forms-api/fetch-single.html) |
| [Get Leave Requests](actions/get-leave-requests.md) | `GET /api/v3/leave-tracker/leaves` | [docs](https://www.zoho.com/people/api/v3/leave-tracker/get-leave.html) |
| [Get Leave Type Summary](actions/get-leave-type-summary.md) | `GET /api/v3/leave-tracker/reports/leave-type-summary/:leaveTypeId` | [docs](https://www.zoho.com/people/api/v3/leave/reports/leave-type-summary.html) |
| [Get Organization Info](actions/get-organization-info.md) | `GET /api/v3/organization` | [docs](https://www.zoho.com/people/api/Organization/Get-details-api.html) |
| [Get Record Count](actions/get-record-count.md) | `GET /api/forms/:formLinkName/getRecordCount` | [docs](https://www.zoho.com/people/api/get-record-count.html) |
| [Get Related Form Records](actions/get-related-form-records.md) | `GET /api/forms/:formLinkName/getRelatedRecords` | [docs](https://www.zoho.com/people/api/forms-api/get-single.html) |
| [Get Specific Attendance Entry](actions/get-specific-attendance-entry.md) | `GET /api/v3/attendance/entries/:entryId` | [docs](https://www.zoho.com/people/api/v3/attendance/entries/get-specific.html) |
| [Get Specific Leave Request](actions/get-specific-leave-request.md) | `GET /api/v3/leave-tracker/leaves/:recordId` | [docs](https://www.zoho.com/people/api/v3/leave-tracker/specificleave.html) |
| [List Form Records](actions/list-form-records.md) | `GET /api/forms/:formLinkName/getRecords` | [docs](https://www.zoho.com/people/api/bulk-records.html) |
| [List Form Views](actions/list-form-views.md) | `GET /api/forms/:formLinkName/views` | [docs](https://www.zoho.com/people/api/fetch-view.html) |
| [List Forms](actions/list-forms.md) | `GET /api/forms` | [docs](https://www.zoho.com/people/api/forms-api/fetch-forms.html) |
| [List Views](actions/list-views.md) | `GET /api/views` | [docs](https://www.zoho.com/people/api/default-custom-views.html) |
| [Search Form Records](actions/search-form-records.md) | `GET /api/forms/:formLinkName/getRecords` | [docs](https://www.zoho.com/people/api/forms-api/search-record.html) |
| [Update Form Record](actions/update-form-record.md) | `POST /api/forms/json/:formLinkName/updateRecord` | [docs](https://www.zoho.com/people/api/update-records.html) |
| [Update Leave Request](actions/update-leave-request.md) | `PUT /api/v3/leave-tracker/leaves/:leaveRecordId` | [docs](https://www.zoho.com/people/api/v3/leave-tracker/edit-leave.html) |
