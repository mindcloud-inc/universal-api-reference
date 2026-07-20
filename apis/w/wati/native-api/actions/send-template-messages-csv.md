# Send Template Messages CSV with Wati

Sends template messages from a CSV file in Wati.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/sendTemplateMessageCSV`
- **Base URL:** `{apiEndpointUrl}`
- **Official documentation:** [Send Template Messages CSV](https://docs.wati.io/reference/post_api-v1-sendtemplatemessagecsv)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `template_name` | query | `string` | yes | Approved Wati template name. |
| `broadcast_name` | query | `string` | yes | Name for the broadcast record. |
| `whatsapp_numbers_csv` | body | `file` | yes | CSV file containing recipient phone numbers. |
