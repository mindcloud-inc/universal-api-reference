# Dropbox Sign: Native API Reference

A consolidated summary of Dropbox Sign's API configuration and 22 documented operations, with links to official documentation.

- **Official docs:** https://developers.hellosign.com/api/api-reference-welcome
- **OpenAPI specification:** https://raw.githubusercontent.com/hellosign/hellosign-openapi/main/openapi.yaml
- **API base URL:** `https://api.hellosign.com/v3`

## Authentication

### API Key

Use your Dropbox Sign API key as the Basic auth username. Leave password blank.

### Credentials

- **Username:** `username` · required
- **Password:** `password` · required

Join the username and password with a colon, Base64-encode the result, and send it with the `Basic` authorization scheme:

```js
const credentials = Buffer.from(`${username}:${password}`).toString('base64');

const response = await fetch(url, {
  headers: {
    Authorization: `Basic ${credentials}`
  }
});
```

[Official authentication documentation](https://developers.hellosign.com/api/reference/authentication/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. The total page count is read from `listInfo.numPages`. The current page number is read from `listInfo.page`.

## Pagination

Use `page_size` in the query string to set the page size. Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (22 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Cancel Signature Request](actions/cancel-signature-request.md) | `POST /signature_request/cancel/:signature_request_id` | [docs](https://developers.hellosign.com/api/reference/operation/signatureRequestCancel/) |
| [Create Template](actions/create-template.md) | `POST /template/create` | [docs](https://developers.hellosign.com/api/template/create) |
| [Get Account](actions/get-account.md) | `GET /account` | [docs](https://developers.hellosign.com/api/reference/operation/accountGet/) |
| [Get API App](actions/get-api-app.md) | `GET /api_app/:client_id` | [docs](https://developers.hellosign.com/api/reference/operation/apiAppGet/) |
| [Get Bulk Send Job](actions/get-bulk-send-job.md) | `GET /bulk_send_job/:bulk_send_job_id` | [docs](https://developers.hellosign.com/api/reference/operation/bulkSendJobGet/) |
| [Get Embedded Sign URL](actions/get-embedded-sign-url.md) | `GET /embedded/sign_url/:signature_id` | [docs](https://developers.hellosign.com/api/reference/operation/embeddedSignUrl/) |
| [Get Embedded Template Edit URL](actions/get-embedded-template-edit-url.md) | `POST /embedded/edit_url/:template_id` | [docs](https://developers.hellosign.com/api/reference/operation/embeddedEditUrl/) |
| [Get Signature Request](actions/get-signature-request.md) | `GET /signature_request/:signature_request_id` | [docs](https://developers.hellosign.com/api/reference/operation/signatureRequestGet/) |
| [Get Signature Request Files](actions/get-signature-request-files.md) | `GET /signature_request/files/:signature_request_id` | [docs](https://developers.hellosign.com/api/reference/operation/signatureRequestFiles/) |
| [Get Signature Request Files as Data URI](actions/get-signature-request-files-as-data-uri.md) | `GET /signature_request/files_as_data_uri/:signature_request_id` | [docs](https://developers.hellosign.com/api/reference/operation/signatureRequestFilesAsDataUri/) |
| [Get Signature Request Files as File URL](actions/get-signature-request-files-as-file-url.md) | `GET /signature_request/files_as_file_url/:signature_request_id` | [docs](https://developers.hellosign.com/api/reference/operation/signatureRequestFilesAsFileUrl/) |
| [Get Template](actions/get-template.md) | `GET /template/:template_id` | [docs](https://developers.hellosign.com/api/reference/operation/templateGet/) |
| [Get Template Files](actions/get-template-files.md) | `GET /template/files/:template_id` | [docs](https://developers.hellosign.com/api/reference/operation/templateFiles/) |
| [Get Template Files as Data URI](actions/get-template-files-as-data-uri.md) | `GET /template/files_as_data_uri/:template_id` | [docs](https://developers.hellosign.com/api/reference/operation/templateFilesAsDataUri/) |
| [Get Template Files as File URL](actions/get-template-files-as-file-url.md) | `GET /template/files_as_file_url/:template_id` | [docs](https://developers.hellosign.com/api/reference/operation/templateFilesAsFileUrl/) |
| [List API Apps](actions/list-api-apps.md) | `GET /api_app/list` | [docs](https://developers.hellosign.com/api/reference/operation/apiAppList/) |
| [List Bulk Send Jobs](actions/list-bulk-send-jobs.md) | `GET /bulk_send_job/list` | [docs](https://developers.hellosign.com/api/reference/operation/bulkSendJobList/) |
| [List Signature Requests](actions/list-signature-requests.md) | `GET /signature_request/list` | [docs](https://developers.hellosign.com/api/reference/operation/signatureRequestList/) |
| [List Templates](actions/list-templates.md) | `GET /template/list` | [docs](https://developers.hellosign.com/api/reference/operation/templateList/) |
| [Send Signature Request](actions/send-signature-request.md) | `POST /signature_request/send` | [docs](https://developers.hellosign.com/api/reference/operation/signatureRequestSend/) |
| [Send Signature Request Reminder](actions/send-signature-request-reminder.md) | `POST /signature_request/remind/:signature_request_id` | [docs](https://developers.hellosign.com/api/reference/operation/signatureRequestRemind/) |
| [Send Signature Request with Template](actions/send-signature-request-with-template.md) | `POST /signature_request/send_with_template` | [docs](https://developers.hellosign.com/api/reference/operation/signatureRequestSendWithTemplate/) |
