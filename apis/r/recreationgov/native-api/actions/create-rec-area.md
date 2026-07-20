# Create Rec Area with Recreation.gov

Creates a new recreation area in Recreation.gov.

## Endpoint

- **Method:** `POST`
- **Path:** `/recareas`
- **Base URL:** `https://ridb.recreation.gov/api/v1`
- **Official documentation:** [Create Rec Area](https://ridb.recreation.gov/shared/swagger/dataSteward.yaml)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `orgId` | body | `number` | no |
| `orgRefId` | body | `string` | no |
| `name` | body | `string` | yes |
| `description` | body | `string` | yes |
| `feeDescription` | body | `string` | no |
| `directions` | body | `string` | yes |
| `accessibilityText` | body | `string` | no |
| `phone` | body | `string` | no |
| `email` | body | `string` | no |
| `reservationUrl` | body | `string` | no |
| `mapUrl` | body | `string` | no |
| `longitude` | body | `number` | no |
| `latitude` | body | `number` | no |
| `stayLimit` | body | `string` | no |
| `enabled` | body | `boolean` | no |
| `reservable` | body | `boolean` | no |
| `keywords` | body | `string` | no |
