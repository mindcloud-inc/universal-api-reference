# Upload Campaign Contacts with Let's Calendar

Uploads campaign contacts to Let's Calendar from CSV or Excel.

## Endpoint

- **Method:** `POST`
- **Path:** `upload-contacts`
- **Base URL:** `https://panel.letscalendar.com/api/lc`
- **Official documentation:** [Upload Campaign Contacts](https://panel.letscalendar.com/docs#apis-POSTapi-lc-upload-contacts)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaign_id` | body | `string` | yes | The unique identifier of the campaign. |
| `file` | body | `file` | yes | CSV or Excel file with contact data. |
| `allow_duplicates` | body | `boolean` | no | Whether to allow duplicate emails. |
