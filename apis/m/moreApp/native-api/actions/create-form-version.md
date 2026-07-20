# Create Form Version with MoreApp

Creates a form version in MoreApp.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1.0/forms/customer/{{customerId}}/forms/{{formId}}/versions`
- **Base URL:** `https://api.moreapp.com`
- **Official documentation:** [Create Form Version](https://docs.moreapp.com/docs/developer-docs/52fae54761987-create-form-version)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customerId` | path | `number` | yes | — |
| `formId` | path | `string` | yes | — |
| `brandingId` | query | `string` | no | — |
| `id` | body | `string` | yes | — |
| `fields[]` | body | `array<object>` | yes | — |
| `variables[]` | body | `array<object>` | yes | Variables array for the form version. |
| `rules[]` | body | `array<object>` | yes | — |
| `triggers[]` | body | `array<object>` | yes | — |
| `integrations[]` | body | `array<object>` | yes | — |
| `settings.interaction` | body | `string` | yes | — |
| `dependencies[]` | body | `array<object>` | yes | Dependencies array for the form version. |
| `settings.saveMode` | body | `string` | yes | — |
| `fieldProperties` | body | `object` | yes | Field properties map for the form version. |
| `settings.icon` | body | `string` | yes | — |
| `theme.id` | body | `string` | yes | — |
| `settings.searchSettings.enabled` | body | `boolean` | yes | — |
| `settings.searchSettings.fields` | body | `object` | yes | — |
| `formId` | body | `string` | no | Form ID in the request body. |
