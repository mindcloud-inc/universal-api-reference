# Export Reports with Expensify

Retrieves exported reports from Expensify.

## Endpoint

- **Method:** `POST`
- **Path:** `ExpensifyIntegrations`
- **Base URL:** `https://integrations.expensify.com/Integration-Server/`
- **Official documentation:** [Export Reports](https://integrations.expensify.com/Integration-Server/doc/#report-exporter)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filtersJson` | body | `string` | yes | JSON object of combinedReportData filters. |
| `fileExtension` | body | `string` | yes | The output file extension. Accepted values: `0`, `1`, `2`, `3`, `4`. |
| `template` | body | `string` | yes | Freemarker template string used to render the exported report file. |
