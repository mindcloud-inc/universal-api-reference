# Remove Bulk Email Finder List with Clearout

Deletes a bulk email finder list from Clearout.

## Endpoint

- **Method:** `POST`
- **Path:** `/email_finder/list/remove`
- **Base URL:** `https://api.clearout.io/v2`
- **Official documentation:** [Remove Bulk Email Finder List](https://docs.clearout.io/developers/api/email-finder)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `list_id` | body | `string` | yes | Pass the value of bulk list_id property from response object |
| `ignore_result` | body | `boolean` | no | Set this value to true when download request is in progress, otherwise list removal will be denied |
