# Create Leave with Timeular

Creates a new leave request in your Timeular workspace.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v4/leaves`
- **Base URL:** `https://api.early.app`
- **Official documentation:** [Create Leave](https://developers.early.app/#ea85a312-9df6-4248-a6ab-3fabec54360b)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `endDate` | body | `string` | yes |
| `note` | body | `string` | no |
| `startDate` | body | `string` | yes |
| `typeId` | body | `string` | yes |
