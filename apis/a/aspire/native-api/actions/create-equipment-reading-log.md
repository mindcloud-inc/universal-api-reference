# Create Equipment Reading Log with Aspire

Creates a new equipment reading log in your Aspire account.

## Endpoint

- **Method:** `POST`
- **Path:** `EquipmentReadingLogs`
- **Base URL:** `https://{environment}.youraspire.com/`
- **Official documentation:** [Create Equipment Reading Log](https://cloud-api.youraspire.com/swagger/index.html#/EquipmentReadingLogs/EquipmentReadingLogs_Create)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `EquipmentID` | body | `number` | no |
| `LogDate` | body | `date` | yes |
| `ReadingDate` | body | `date` | yes |
| `MeterReading` | body | `number` | yes |
| `TroubleCode` | body | `string` | no |
