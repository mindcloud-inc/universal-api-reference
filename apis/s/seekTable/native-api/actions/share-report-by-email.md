# Share Report By Email with SeekTable

Shares a SeekTable report by email.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/report/:report_id/share/email`
- **Base URL:** `https://www.seektable.com`
- **Official documentation:** [Share Report By Email](https://www.seektable.com/help/web-api-integration)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `report_id` | path | `string` | yes | GUID of the report saved in your SeekTable account. |
| `to` | body | `string` | yes | Email address of the recipient. |
| `subject` | body | `string` | yes | Email subject line. |
| `message` | body | `string` | no | Additional text included in the email body. |
| `include_report_html` | body | `boolean` | no | Whether the report HTML should be included directly in the email body. |
| `attach_export` | body | `string` | no | Comma-separated list of export types to attach to the email. |
| `report_parameters` | body | `string` | no | JSON object string with report parameter values. Requires Advanced Publishing. |
