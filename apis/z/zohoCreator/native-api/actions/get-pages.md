# Get Pages with Zoho Creator

Retrieves pages from a Zoho Creator application.

## Endpoint

- **Method:** `GET`
- **Path:** `/meta/:account_owner_name/:app_link_name/pages`
- **Base URL:** `https://www.zohoapis.com/creator/v2.1`
- **Official documentation:** [Get Pages](https://www.zoho.com/creator/help/api/v2.1/get-pages.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `account_owner_name` | path | `string` | yes | Zoho Creator account owner name. |
| `app_link_name` | path | `string` | yes | Zoho Creator app link name. |
