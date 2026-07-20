# Create alert with Atera

Creates an alert in Atera.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v3/alerts`
- **Base URL:** `https://app.atera.com`
- **Official documentation:** [Create alert](https://app.atera.com/apidocs#!/Alert/Alert_Post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `AdditionalInfo` | body | `string` | no | Additional alert details. |
| `AlertCategoryID` | body | `string` | no | Alert category. |
| `Code` | body | `number` | no | Alert code. |
| `CustomerID` | body | `number` | yes | Customer ID for the alert. |
| `DeviceGuid` | body | `string` | yes | Global unique device identifier. |
| `FolderID` | body | `number` | no | Folder ID. |
| `MessageTemplate` | body | `string` | no | Alert message template. |
| `Severity` | body | `string` | no | Alert severity. |
| `SnoozedEndDate` | body | `string` | no | UTC snooze end timestamp. |
| `ThresholdValue1` | body | `string` | no | First threshold value. |
| `ThresholdValue2` | body | `string` | no | Second threshold value. |
| `ThresholdValue3` | body | `string` | no | Third threshold value. |
| `ThresholdValue4` | body | `string` | no | Fourth threshold value. |
| `ThresholdValue5` | body | `string` | no | Fifth threshold value. |
| `TicketID` | body | `number` | no | Related ticket ID. |
| `Title` | body | `string` | yes | Alert title. |
