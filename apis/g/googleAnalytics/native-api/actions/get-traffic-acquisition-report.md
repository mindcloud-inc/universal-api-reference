# Get Traffic Acquisition Report with Google Analytics

## Endpoint

- **Method:** `POST`
- **Path:** `https://analyticsdata.googleapis.com/v1beta/properties/:propertyId:urlEnd`
- **Base URL:** `https://analyticsdata.googleapis.com/v1beta`
- **Official documentation:** [Get Traffic Acquisition Report](https://developers.google.com/analytics/devguides/reporting/data/v1/rest/v1beta/properties/runReport)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `propertyId` | path | `string` | yes | GA4 property ID without the properties/ prefix |
| `dateRanges[]` | body | `array<object>` | yes | — |
| `limit` | body | `number` | no | — |
| `offset` | body | `number` | no | — |
