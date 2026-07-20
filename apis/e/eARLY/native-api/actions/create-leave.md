# Create Leave with EARLY

Creates a new leave in EARLY.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v4/leaves`
- **Base URL:** `https://api.early.app`
- **Official documentation:** [Create Leave](https://developers.early.app/#ea85a312-9df6-4248-a6ab-3fabec54360b)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `typeId` | body | `string` | yes | Leave type ID. |
| `startDate` | body | `string` | yes | Leave start timestamp. |
| `endDate` | body | `string` | yes | Leave end timestamp. |
| `note` | body | `string` | no | Optional leave note. |
