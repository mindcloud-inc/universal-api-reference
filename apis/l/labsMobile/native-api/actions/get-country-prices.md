# Get Country Prices with LabsMobile

Retrieves SMS prices for specific countries from LabsMobile.

## Endpoint

- **Method:** `POST`
- **Path:** `/json/prices`
- **Base URL:** `https://api.labsmobile.com`
- **Official documentation:** [Get Country Prices](https://www.labsmobile.com/en/sms-api/api-versions/http-rest-post-json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `countries[]` | body | `array<string>` | yes | Country ISO code array. |
