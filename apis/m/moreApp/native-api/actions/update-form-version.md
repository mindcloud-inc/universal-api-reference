# Update Form Version with MoreApp

Updates a form version in MoreApp.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/v1.0/forms/customer/{{customerId}}/forms/{{formId}}/versions/{{formVersionId}}`
- **Base URL:** `https://api.moreapp.com`
- **Official documentation:** [Update Form Version](https://docs.moreapp.com/docs/developer-docs/6e4778ea3dc32-update-form-version)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `customerId` | path | `number` | yes |
| `formId` | path | `string` | yes |
| `formVersionId` | path | `string` | yes |
| `id` | body | `string` | yes |
| `formId` | body | `string` | yes |
| `fields[]` | body | `array<object>` | yes |
| `variables[]` | body | `array<object>` | yes |
| `rules[]` | body | `array<object>` | yes |
| `triggers[]` | body | `array<object>` | yes |
| `integrations[]` | body | `array<object>` | yes |
| `dependencies[]` | body | `array<object>` | yes |
| `fieldProperties` | body | `object` | yes |
| `settings.interaction` | body | `string` | yes |
| `settings.saveMode` | body | `string` | yes |
| `settings.icon` | body | `string` | yes |
| `theme.id` | body | `string` | yes |
| `settings.searchSettings.enabled` | body | `boolean` | yes |
| `settings.searchSettings.fields` | body | `object` | yes |
