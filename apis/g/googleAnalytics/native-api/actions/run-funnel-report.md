# Run Funnel Report with Google Analytics

## Endpoint

- **Method:** `POST`
- **Path:** `https://analyticsdata.googleapis.com/v1alpha/properties/:propertyId:urlEnd`
- **Base URL:** `https://analyticsdata.googleapis.com/v1beta`
- **Official documentation:** [Run Funnel Report](https://developers.google.com/analytics/devguides/reporting/data/v1/rest/v1alpha/properties/runFunnelReport)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `propertyId` | path | `string` | yes | GA4 property ID without the properties/ prefix |
| `dateRanges[]` | body | `array<object>` | yes | — |
| `funnel` | body | `object` | yes | Early-preview GA4 funnel definition containing ordered funnel steps |
| `limit` | body | `number` | no | — |
