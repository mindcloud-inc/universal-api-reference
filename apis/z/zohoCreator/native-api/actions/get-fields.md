# Get Fields with Zoho Creator

Retrieves fields from a Zoho Creator form.

## Endpoint

- **Method:** `GET`
- **Path:** `/meta/:account_owner_name/:app_link_name/form/:form_link_name/fields`
- **Base URL:** `https://www.zohoapis.com/creator/v2.1`
- **Official documentation:** [Get Fields](https://www.zoho.com/creator/help/api/v2.1/get-fields.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `account_owner_name` | path | `string` | yes | Zoho Creator account owner name. |
| `app_link_name` | path | `string` | yes | Zoho Creator app link name. |
| `form_link_name` | path | `string` | yes | Zoho Creator form link name. |
