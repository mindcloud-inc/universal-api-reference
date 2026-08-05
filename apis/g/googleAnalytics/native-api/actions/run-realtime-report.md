# Run Realtime Report with Google Analytics

## Endpoint

- **Method:** `POST`
- **Path:** `https://analyticsdata.googleapis.com/v1beta/properties/:propertyId:urlEnd`
- **Base URL:** `https://analyticsdata.googleapis.com/v1beta`
- **Official documentation:** [Run Realtime Report](https://developers.google.com/analytics/devguides/reporting/data/v1/rest/v1beta/properties/runRealtimeReport)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `propertyId` | path | `string` | yes | GA4 property ID without the properties/ prefix |
| `limit` | body | `number` | no | Maximum report rows to return |
| `offset` | body | `number` | no | Zero-based row offset |
