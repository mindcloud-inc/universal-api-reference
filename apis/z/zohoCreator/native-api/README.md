# Zoho Creator: Native API Reference

A consolidated summary of Zoho Creator's API configuration and 23 documented operations, with links to official documentation.

- **Official docs:** https://www.zoho.com/creator/help/api/v2.1/
- **OpenAPI specification:** https://creator.zoho.com/api/v2.1/downloadOAS
- **API base URL:** `https://www.zohoapis.com/creator/v2.1`

## Authentication

### OAuth2

Connect Zoho Creator with OAuth 2.0

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://accounts.zoho.com/oauth/v2/auth to approve access.
2. Exchange the returned authorization code with a POST request to https://accounts.zoho.com/oauth/v2/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `ZohoCreator.form.CREATE ZohoCreator.report.CREATE ZohoCreator.report.READ ZohoCreator.report.UPDATE ZohoCreator.report.DELETE ZohoCreator.meta.form.READ ZohoCreator.meta.application.READ ZohoCreator.dashboard.READ ZohoCreator.bulk.CREATE ZohoCreator.bulk.READ`.

The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://accounts.zoho.com/oauth/v2/token.

[Official authentication documentation](https://www.zoho.com/creator/help/api/v2.1/oauth-overview.html)

## Endpoints (23 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Records](actions/add-records.md) | `POST /data/:account_owner_name/:app_link_name/form/:form_link_name` | [docs](https://www.zoho.com/creator/help/api/v2.1/add-records.html) |
| [Create Bulk Read Job](actions/create-bulk-read-job.md) | `POST /bulk/:account_owner_name/:app_link_name/report/:report_link_name/read` | [docs](https://www.zoho.com/creator/help/api/v2.1/bulk-api/create-bulk-read-job.html) |
| [Delete Record by ID](actions/delete-record-by-id.md) | `DELETE /data/:account_owner_name/:app_link_name/report/:report_link_name/:record_ID` | [docs](https://www.zoho.com/creator/help/api/v2.1/delete-specific-record.html) |
| [Delete Records](actions/delete-records.md) | `DELETE /data/:account_owner_name/:app_link_name/report/:report_link_name` | [docs](https://www.zoho.com/creator/help/api/v2.1/delete-records.html) |
| [Download Bulk Read Result](actions/download-bulk-read-result.md) | `GET /bulk/:account_owner_name/:app_link_name/report/:report_link_name/read/:job_ID/result` | [docs](https://www.zoho.com/creator/help/api/v2.1/bulk-api/download-bulk-read-result.html) |
| [Download File](actions/download-file.md) | `GET /data/:account_owner_name/:app_link_name/report/:report_link_name/:record_ID/:field_link_name/download` | [docs](https://www.zoho.com/creator/help/api/v2.1/download-file.html) |
| [Download File from Subform](actions/download-file-from-subform.md) | `GET /data/:account_owner_name/:app_link_name/report/:report_link_name/:record_ID/:subform_link_name/:field_link_name/:subform_record_ID/download` | [docs](https://www.zoho.com/creator/help/api/v2.1/download-file-from-subform.html) |
| [Get Applications](actions/get-applications.md) | `GET /meta/applications` | [docs](https://www.zoho.com/creator/help/api/v2.1/get-workspace-applications.html) |
| [Get Applications by Workspace](actions/get-applications-by-workspace.md) | `GET /meta/:account_owner_name/applications` | [docs](https://www.zoho.com/creator/help/api/v2.1/get-applications.html) |
| [Get Bulk Read Job Status](actions/get-bulk-read-job-status.md) | `GET /bulk/:account_owner_name/:app_link_name/report/:report_link_name/read/:job_ID` | [docs](https://www.zoho.com/creator/help/api/v2.1/bulk-api/get-the-status-of-the-bulk-read-job.html) |
| [Get Fields](actions/get-fields.md) | `GET /meta/:account_owner_name/:app_link_name/form/:form_link_name/fields` | [docs](https://www.zoho.com/creator/help/api/v2.1/get-fields.html) |
| [Get Forms](actions/get-forms.md) | `GET /meta/:account_owner_name/:app_link_name/forms` | [docs](https://www.zoho.com/creator/help/api/v2.1/get-forms.html) |
| [Get Pages](actions/get-pages.md) | `GET /meta/:account_owner_name/:app_link_name/pages` | [docs](https://www.zoho.com/creator/help/api/v2.1/get-pages.html) |
| [Get Record by ID](actions/get-record-by-id.md) | `GET /data/:account_owner_name/:app_link_name/report/:report_link_name/:record_ID` | [docs](https://www.zoho.com/creator/help/api/v2.1/get-records-by-ID.html) |
| [Get Records](actions/get-records.md) | `GET /data/:account_owner_name/:app_link_name/report/:report_link_name` | [docs](https://www.zoho.com/creator/help/api/v2.1/get-records.html) |
| [Get Reports](actions/get-reports.md) | `GET /meta/:account_owner_name/:app_link_name/reports` | [docs](https://www.zoho.com/creator/help/api/v2.1/get-reports.html) |
| [Get Sections](actions/get-sections.md) | `GET /meta/:account_owner_name/:app_link_name/sections` | [docs](https://www.zoho.com/creator/help/api/v2.1/get-sections.html) |
| [Publish Add Records](actions/publish-add-records.md) | `POST /publish/:account_owner_name/:app_link_name/form/:form_link_name` | [docs](https://www.zoho.com/creator/help/api/v2.1/publish-api/add-records.html) |
| [Publish Get Record by ID](actions/publish-get-record-by-id.md) | `GET /publish/:account_owner_name/:app_link_name/report/:report_link_name/:record_ID` | [docs](https://www.zoho.com/creator/help/api/v2.1/publish-api/get-record-by-id.html) |
| [Publish Get Records](actions/publish-get-records.md) | `GET /publish/:account_owner_name/:app_link_name/report/:report_link_name` | [docs](https://www.zoho.com/creator/help/api/v2.1/publish-api/get-records.html) |
| [Update Record by ID](actions/update-record-by-id.md) | `PATCH /data/:account_owner_name/:app_link_name/report/:report_link_name/:record_ID` | [docs](https://www.zoho.com/creator/help/api/v2.1/update-specific-record.html) |
| [Update Records](actions/update-records.md) | `PATCH /data/:account_owner_name/:app_link_name/report/:report_link_name` | [docs](https://www.zoho.com/creator/help/api/v2.1/update-records.html) |
| [Upload File](actions/upload-file.md) | `POST /data/:account_owner_name/:app_link_name/report/:report_link_name/:record_ID/:field_link_name/upload` | [docs](https://www.zoho.com/creator/help/api/v2.1/upload-file.html) |
