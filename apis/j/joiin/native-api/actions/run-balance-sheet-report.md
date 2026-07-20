# Run Balance Sheet Report with Joiin

Retrieves a balance sheet report from Joiin.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/report/balance-sheet`
- **Base URL:** `https://app-api.joiin.co`
- **Official documentation:** [Run Balance Sheet Report](https://app.joiin.co/reference/run_balance_sheet_report)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `startDate` | body | `date` | yes | The report start date in YYYY-MM format. |
| `endDate` | body | `date` | yes | The report end date in YYYY-MM format. |
| `currency` | body | `string` | yes | The report currency code, for example USD. |
| `companies[]` | body | `array<string>` | yes | A list of company IDs or company names to include in the report. |
| `eliminationSet` | body | `string` | no | The elimination set to use for the report. |
| `eliminationType` | body | `string` | no | How Joiin should apply eliminations for the report. |
| `budget` | body | `boolean` | no | Whether to include budget data in the report. |
| `displayOptions` | body | `object` | no | Display options for the report response. |
| `breakdown` | body | `string` | no | The period breakdown to use for the report. |
