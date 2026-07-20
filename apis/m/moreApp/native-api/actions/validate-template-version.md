# Validate Template Version with MoreApp

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1.0/forms/customer/{{customerId}}/templates/{{formId}}/versions/validate`
- **Base URL:** `https://api.moreapp.com`
- **Official documentation:** [Validate Template Version](https://docs.moreapp.com/docs/developer-docs/a10fa9e66b164-get-versions-of-a-template)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `customerId` | path | `number` | yes |
| `formId` | path | `string` | yes |
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
