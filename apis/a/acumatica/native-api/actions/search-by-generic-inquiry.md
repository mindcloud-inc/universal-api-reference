# Search By Generic Inquiry with Acumatica

Search the 'Default' Acumatica Endpoint for a Generic Inquiry.
This need to be a PUT

## Endpoint

- **Method:** `GET`
- **Path:** `/t/{tenant}/api/odata/gi/:entity`
- **Base URL:** `{uRL}`
- **Official documentation:** [Search By Generic Inquiry](https://beacon.acumatica.com/r/Reporting-Tools-Guide/Managing-Generic-Inquiries/Accessing-the-Exposed-Inquiry-Results-Through-OData/Generic-Inquiry-Access-Through-OData-To-Retrieve-Data-by-Using-a-Custom-Generic-Inquiry?contentId=cc82rZNDKqRONoGHOP9z6w)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Body` | body | `object` | no | — |
| `$expand` | query | `string` | no | Use the expand parameter to specify linked and detail entities that should be expanded. By default, no linked or detail entities are expanded; that is, only fields of the top-level entity are returned. You need to explicitly specify each linked or detail entity to be expanded. (Example: to expand the Project Attributes use $expand=Attributes). Send multiple values as a array. |
| `$filter` | query | `string` | no | Use the $filter parameter to specify conditions that determine which records should be returned from Acumatica ERP. |
| `$select` | query | `string` | no | When you retrieve records from Acumatica ERP you use the $select parameter to specify the fields of the entity to be returned. By default, ALL fields of the entity are returned. Send multiple values as a array. |
| `entity` | path | `string<string>` | yes | The OData EntitySet name of a Generic Inquiry that has Expose via OData enabled. Accepted values: `Contacts`, `Customer`, `ProFormaInvoice`, `Project`, `ProjectActivity`, `ProjectBudget`, `ProjectEmployee`, `ProjectEquipment`, `ProjectRetainage`, `ProjectTask`, `ProjectTransaction`, `SalesOrder`. |
| `$custom` | query | `string` | no | Specify the fields that are not defined in the contract to be returned. For details, see $custom Parameter. |
