# Create Property Availability with Aspire

Creates a new property availability in your Aspire account.

## Endpoint

- **Method:** `POST`
- **Path:** `PropertyAvailabilities`
- **Base URL:** `https://{environment}.youraspire.com/`
- **Official documentation:** [Create Property Availability](https://cloud-api.youraspire.com/swagger/index.html#/PropertyAvailabilities/PropertyAvailabilities_Create)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `AvailabilityTimes[]` | body | `array<object>` | no |
| `PropertyId` | body | `number` | yes |
