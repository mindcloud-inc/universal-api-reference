# Publish Add Records with Zoho Creator

Creates new records through a Zoho Creator publish form.

## Endpoint

- **Method:** `POST`
- **Path:** `/publish/:account_owner_name/:app_link_name/form/:form_link_name`
- **Base URL:** `https://www.zohoapis.com/creator/v2.1`
- **Official documentation:** [Publish Add Records](https://www.zoho.com/creator/help/api/v2.1/publish-api/add-records.html)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `account_owner_name` | path | `string` | yes | Zoho Creator account owner name. |
| `app_link_name` | path | `string` | yes | Zoho Creator app link name. |
| `form_link_name` | path | `string` | yes | Zoho Creator form link name. |
| `privatelink` | query | `string` | yes | Zoho Creator publish API private link token. |
| `result` | body | `object` | no | Response result preferences. |
| `data[]` | body | `array<object>` | yes | Array of record objects to create through the publish API. |
