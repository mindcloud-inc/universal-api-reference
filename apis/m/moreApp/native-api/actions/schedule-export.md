# Schedule Export with MoreApp

Schedules a submission export in MoreApp.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1.0/customers/{{customerId}}/forms/{{formId}}/submissions/export`
- **Base URL:** `https://api.moreapp.com`
- **Official documentation:** [Schedule Export](https://docs.moreapp.com/docs/developer-docs/45b37124ae038-schedule-an-export)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `customerId` | path | `number` | yes |
| `formId` | path | `string` | yes |
| `exporterType` | body | `string` | yes |
| `mailOnFinish[]` | body | `array<string>` | yes |
| `submissionIds[]` | body | `array<string>` | yes |
| `options.timezone` | body | `string` | yes |
| `options.languageCode` | body | `string` | yes |
| `exportFields[]` | body | `array<object>` | yes |
