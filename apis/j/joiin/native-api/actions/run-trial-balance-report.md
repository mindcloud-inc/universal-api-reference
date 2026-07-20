# Run Trial Balance Report with Joiin

Retrieves a trial balance report from Joiin.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/report/trial-balance`
- **Base URL:** `https://app-api.joiin.co`
- **Official documentation:** [Run Trial Balance Report](https://app.joiin.co/reference/run_trial_balance_report)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `startDate` | body | `date` | yes | The report start date in YYYY-MM format. |
| `endDate` | body | `date` | yes | The report end date in YYYY-MM format. |
| `currency` | body | `string` | yes | The report currency code, for example USD. |
| `companies[]` | body | `array<string>` | yes | A list of company IDs or company names to include in the report. |
| `eliminationSet` | body | `string` | no | The elimination set to use for the report. |
| `eliminationType` | body | `string` | no | How Joiin should apply eliminations for the report. |
| `periodNumber` | body | `number` | no | The period number to use for the trial balance report. |
