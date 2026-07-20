# List All Contacts with Freshsales Classic

Retrieves contacts from a Freshsales Classic view.

## Endpoint

- **Method:** `GET`
- **Path:** `/contacts/view/:viewId`
- **Base URL:** `https://{bundleAlias}/api`
- **Official documentation:** [List All Contacts](https://developers.freshworks.com/crm/api/#list_all_contacts)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page` | query | `number` | no | Page number to return for the selected contact view. |
| `viewId` | path | `number` | yes | The contact view ID. |
