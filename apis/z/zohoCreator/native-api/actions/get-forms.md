# Get Forms with Zoho Creator

Retrieves forms from a Zoho Creator application.

## Endpoint

- **Method:** `GET`
- **Path:** `/meta/:account_owner_name/:app_link_name/forms`
- **Base URL:** `https://www.zohoapis.com/creator/v2.1`
- **Official documentation:** [Get Forms](https://www.zoho.com/creator/help/api/v2.1/get-forms.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `account_owner_name` | path | `string` | yes | Zoho Creator account owner name. |
| `app_link_name` | path | `string` | yes | Zoho Creator app link name. |
