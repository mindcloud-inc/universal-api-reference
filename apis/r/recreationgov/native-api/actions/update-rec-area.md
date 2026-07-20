# Update Rec Area with Recreation.gov

Updates an existing recreation area in Recreation.gov.

## Endpoint

- **Method:** `PUT`
- **Path:** `/recareas/{id}`
- **Base URL:** `https://ridb.recreation.gov/api/v1`
- **Official documentation:** [Update Rec Area](https://ridb.recreation.gov/shared/swagger/dataSteward.yaml)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `number` | yes |
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
