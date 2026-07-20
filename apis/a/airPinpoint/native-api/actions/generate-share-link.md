# Generate Share Link with AirPinpoint

Creates a temporary share link for a trackable in AirPinpoint.

## Endpoint

- **Method:** `POST`
- **Path:** `/share-links`
- **Base URL:** `https://api.airpinpoint.com/v1`
- **Official documentation:** [Generate Share Link](https://airpinpoint.com/docs/share-links)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `hours` | body | `number` | yes |
| `trackableId` | body | `string` | yes |
