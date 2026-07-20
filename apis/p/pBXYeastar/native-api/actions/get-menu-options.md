# Get Menu Options with PBX Yeastar

Retrieves menu options from PBX Yeastar.

## Endpoint

- **Method:** `GET`
- **Path:** `/system/get_menuoptions`
- **Base URL:** `{baseUrl}/openapi/v1.0`
- **Official documentation:** [Get Menu Options](https://help.yeastar.com/en/p-series-cloud-edition/developer-guide/get-menu-options.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `menu` | query | `string` | yes | Yeastar menu option category to query, such as extension, org_list, trunk, phonebook, queue, or conference. |
