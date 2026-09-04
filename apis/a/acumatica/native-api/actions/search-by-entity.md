# Search By Entity with Acumatica

Search the 'Default' Acumatica Endpoint for a Specific Entity

## Endpoint

- **Method:** `GET`
- **Path:** `/entity/{endpointName}/{endpointVersion}/:entity`
- **Base URL:** `{uRL}`
- **Official documentation:** [Search By Entity](https://help.acumatica.com/(W(5))/Help?ScreenId=ShowWiki&pageid=56831ee7-14b0-45ef-8207-dace30beb2cb)

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
| `$expand` | query | `string` | no | Use the expand parameter to specify linked and detail entities that should be expanded. By default, no linked or detail entities are expanded; that is, only fields of the top-level entity are returned. You need to explicitly specify each linked or detail entity to be expanded. (Example: to expand the Project Attributes use $expand=Attributes). Send multiple values as a array. |
| `$select` | query | `string` | no | When you retrieve records from Acumatica ERP you use the $select parameter to specify the fields of the entity to be returned. By default, ALL fields of the entity are returned. Send multiple values as a array. |
| `entity` | path | `list<string>` | yes | The top-level entity to retrieve. Example: "Project" or "User" Accepted values: `Contacts`, `Customer`, `ProFormaInvoice`, `Project`, `ProjectActivity`, `ProjectBudget`, `ProjectEmployee`, `ProjectEquipment`, `ProjectRetainage`, `ProjectTask`, `ProjectTransaction`, `SalesOrder`. |
| `$filter` | query | `string` | no | Use the $filter parameter to specify conditions that determine which records should be returned from Acumatica ERP. |
| `$custom` | query | `string` | no | Specify the fields that are not defined in the contract to be returned. For details, see $custom Parameter. |
