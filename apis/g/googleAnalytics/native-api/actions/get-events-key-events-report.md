# Get Events and Key Events Report with Google Analytics

## Endpoint

- **Method:** `POST`
- **Path:** `https://analyticsdata.googleapis.com/v1beta/properties/:propertyId:urlEnd`
- **Base URL:** `https://analyticsdata.googleapis.com/v1beta`
- **Official documentation:** [Get Events and Key Events Report](https://developers.google.com/analytics/devguides/reporting/data/v1/rest/v1beta/properties/runReport)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `propertyId` | path | `string` | yes | GA4 property ID without the properties/ prefix |
| `dateRanges[]` | body | `array<object>` | yes | One or more GA4 date ranges. Each item is an object with startDate and endDate keys (for example startDate 30daysAgo, endDate today), not a plain date string. |
| `limit` | body | `number` | no | Maximum report rows to return |
| `offset` | body | `number` | no | Zero-based row offset |
| `dateRanges[].startDate` | body | `string` | yes | Range start as YYYY-MM-DD or a relative value such as 30daysAgo, yesterday, or today |
| `dateRanges[].endDate` | body | `string` | yes | Range end as YYYY-MM-DD or a relative value such as today or yesterday |
