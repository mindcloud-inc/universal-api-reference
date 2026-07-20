# Run Performance Audit with Browserless

Retrieves Lighthouse audit results from Browserless.

## Endpoint

- **Method:** `POST`
- **Path:** `/performance`
- **Base URL:** `https://production-sfo.browserless.io`
- **Official documentation:** [Run Performance Audit](https://docs.browserless.io/rest-apis/performance)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | The URL to analyze with Lighthouse. |
| `config` | body | `object` | no | Optional Lighthouse configuration object passed through to Browserless for audit scoping and settings overrides. |
| `budgets[]` | body | `array<object>` | no | Optional Lighthouse budgets array used to evaluate resource and timing budgets during the audit. |
