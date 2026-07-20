# Fetch Analysis with Humantic AI

## Endpoint

- **Method:** `GET`
- **Path:** `/user-profile/`
- **Base URL:** `https://api.humantic.ai/v1`
- **Official documentation:** [Fetch Analysis](https://api.humantic.ai/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | query | `string` | yes | The same identifier used when the analysis was created. |
| `persona` | query | `string` | no | Optional persona context. Humantic documents `sales` and `hiring`; multiple values can be comma-delimited. Send multiple values as a string separated by `,`. |
| `override` | query | `boolean` | no | When true, Humantic may return results for text input under 300 words; docs warn the results may be inaccurate. |
