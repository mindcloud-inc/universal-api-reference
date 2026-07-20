# Get Campaign Report XLSX Export with SMS Connexion

Retrieves a campaign report export from SMS Connexion as XLSX.

## Endpoint

- **Method:** `GET`
- **Path:** `/reports/campaigns/:campaignId/xlsx`
- **Base URL:** `https://api.sms.cx`
- **Official documentation:** [Get Campaign Report XLSX Export](https://sms.cx/sms-api-documentation/#operation/ExportCampaignReportToXLSX)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaignId` | path | `string` | yes | Campaign UUID from report campaigns endpoints. |
