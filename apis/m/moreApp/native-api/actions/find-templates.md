# Find Templates with MoreApp

Finds templates in MoreApp.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1.0/forms/customer/{{customerId}}/templates`
- **Base URL:** `https://api.moreapp.com`
- **Official documentation:** [Find Templates](https://docs.moreapp.com/docs/developer-docs/0d2f747ca6fa8-find-templates)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `customerId` | path | `number` | yes |
| `page` | query | `number` | no |
| `scope` | query | `string` | no |
| `language` | query | `string` | no |
| `query` | query | `string` | no |
| `tags` | query | `string` | no |
