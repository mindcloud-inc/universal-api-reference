# List Opportunity Attachments with Autotask

## Endpoint

- **Method:** `GET`
- **Path:** `/OpportunityAttachments/query`
- **Base URL:** `https://webservices14.autotask.net/ATServicesRest/v1.0`
- **Official documentation:** [List Opportunity Attachments](https://autotask.net/help/developerhelp/Content/APIs/REST/Entities/OpportunityAttachmentsEntity.htm)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filters[]` | query | `array<object>` | yes | Build one or more Autotask filter conditions. Conditions are combined with AND. |
| `filters[].field` | query | `string` | yes | Autotask entity field name to filter, such as id or companyName. |
| `filters[].operator` | query | `list<string>` | yes | Comparison operator applied between the field and value. Accepted values: `beginsWith`, `contains`, `endsWith`, `eq`, `exist`, `gt`, `gte`, `in`, `lt`, `lte`, `notExist`, `notIn`, `noteq`. |
| `filters[].valueType` | query | `list<string>` | yes | How to encode the filter value. Dates and timestamps should use String with the Autotask-supported format. Accepted values: `boolean`, `number`, `string`. |
| `filters[].value` | query | `string` | no | Value for scalar operators. Leave empty for Exists, Does Not Exist, In, and Not In. |
| `filters[].list[]` | query | `array<string>` | no | Values for In or Not In operators. |
| `filters[].udf` | query | `boolean` | no | Enable when Field names an Autotask user-defined field. |
