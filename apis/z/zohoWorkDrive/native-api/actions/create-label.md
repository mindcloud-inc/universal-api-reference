# Create Label with Zoho WorkDrive

Creates a new label in Zoho WorkDrive.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/labels`
- **Base URL:** `{api_domain}/workdrive`
- **Official documentation:** [Create Label](https://workdrive.zoho.com/apidocs/v1/labels/createlabel)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data.attributes.name` | body | `string` | yes | Display name of the label. |
| `data.attributes.color` | body | `string` | no | Hex color code for the label, without the leading #. |
| `data.attributes.user_id` | body | `string` | yes | Pass the current team member record ID from Get Current Team Member, not the ZUID from Get User Info. |
