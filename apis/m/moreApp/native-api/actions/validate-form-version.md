# Validate Form Version with MoreApp

Validates a form version in MoreApp.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1.0/forms/customer/{{customerId}}/forms/{{formId}}/versions/validate`
- **Base URL:** `https://api.moreapp.com`
- **Official documentation:** [Validate Form Version](https://docs.moreapp.com/docs/developer-docs/0e8bad70e535a-validate-form-version)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `customerId` | path | `number` | yes |
| `formId` | path | `string` | yes |
| `id` | body | `string` | yes |
| `fields[]` | body | `array<object>` | yes |
| `rules[]` | body | `array<object>` | yes |
| `triggers[]` | body | `array<object>` | yes |
| `integrations[]` | body | `array<object>` | yes |
| `settings.interaction` | body | `string` | yes |
| `settings.saveMode` | body | `string` | yes |
| `settings.icon` | body | `string` | yes |
| `theme.id` | body | `string` | yes |
| `settings.searchSettings.enabled` | body | `boolean` | yes |
| `settings.searchSettings.fields` | body | `object` | yes |
