# Update Equipment Reading Log with Aspire

Updates an existing equipment reading log in your Aspire account.

## Endpoint

- **Method:** `PUT`
- **Path:** `EquipmentReadingLogs`
- **Base URL:** `https://{environment}.youraspire.com/`
- **Official documentation:** [Update Equipment Reading Log](https://cloud-api.youraspire.com/swagger/index.html#/EquipmentReadingLogs/EquipmentReadingLogs_Update)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `EquipmentID` | body | `number` | no |
| `LogDate` | body | `date` | yes |
| `ReadingDate` | body | `date` | yes |
| `MeterReading` | body | `number` | yes |
| `TroubleCode` | body | `string` | no |
| `EquipmentReadingLogID` | body | `number` | yes |
