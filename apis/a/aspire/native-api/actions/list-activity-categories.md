# List Activity Categories with Aspire

Activity categories allow you to provide a further descriptive breakdown for issues and tasks (i.e., for an issue, the category could be Complaint or Service Request).

## Endpoint

- **Method:** `GET`
- **Path:** `ActivityCategories`
- **Base URL:** `https://{environment}.youraspire.com/`
- **Official documentation:** [List Activity Categories](https://guide.youraspire.com/apidocs/activitycategories-6)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `$expand` | query | `string` | no |
| `$filter` | query | `string` | no |
| `$orderby` | query | `string` | no |
| `$select` | query | `string` | no |
