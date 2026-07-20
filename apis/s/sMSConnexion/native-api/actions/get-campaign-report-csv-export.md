# Get Campaign Report CSV Export with SMS Connexion

Retrieves a campaign report export from SMS Connexion as CSV.

## Endpoint

- **Method:** `GET`
- **Path:** `/reports/campaigns/:campaignId/csv`
- **Base URL:** `https://api.sms.cx`
- **Official documentation:** [Get Campaign Report CSV Export](https://sms.cx/sms-api-documentation/#operation/ExportCampaignReportToCSV)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaignId` | path | `string` | yes | Campaign UUID from report campaigns endpoints. |
