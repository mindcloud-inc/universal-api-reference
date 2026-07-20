# Get Carbon Intensity By Date and Settlement Period with Carbon Intensity

Retrieves carbon intensity for a date and settlement period.

## Endpoint

- **Method:** `GET`
- **Path:** `/intensity/date/:date/:period`
- **Base URL:** `https://api.carbonintensity.org.uk`
- **Official documentation:** [Get Carbon Intensity By Date and Settlement Period](https://api.carbonintensity.org.uk/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `date` | path | `string` | yes | Date in YYYY-MM-DD format exactly as required by the API path. |
| `period` | path | `number` | yes | Settlement period number for the selected date. |
