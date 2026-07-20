# List Room Calendar with Beds24

Retrieves room calendar values from Beds24.

## Endpoint

- **Method:** `GET`
- **Path:** `/inventory/rooms/calendar`
- **Base URL:** `https://beds24.com/api/v2`
- **Official documentation:** [List Room Calendar](https://wiki.beds24.com/index.php/API_V2.0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `endDate` | query | `string` | yes | Calendar range end date in YYYY-MM-DD format. |
| `startDate` | query | `string` | yes | Calendar range start date in YYYY-MM-DD format. |
