# Get Lead Form Analytic Data with Sakari SMS

Retrieves lead form analytics from Sakari SMS.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/accounts/:accountId/forms/:formId/analytics`
- **Base URL:** `https://api.sakari.io`
- **Official documentation:** [Get Lead Form Analytic Data](https://developer.sakari.io/api-reference/forms/fetch-lead-form-analytic-data)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `formId` | path | `string` | yes | — |
| `start` | query | `string` | no | General search term that specifies start date |
| `end` | query | `string` | no | General search term that specifies end date |
