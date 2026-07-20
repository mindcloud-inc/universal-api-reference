# Enrich Intent with Zoominfo

Enriches company intent data with ZoomInfo data.

## Endpoint

- **Method:** `POST`
- **Path:** `enrich/intent`
- **Base URL:** `https://api.zoominfo.com/`
- **Official documentation:** [Enrich Intent](https://api-docs.zoominfo.com/#48c36a9f-e4eb-4ce8-8080-a7b810df7c2d)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `topics[]` | body | `array<string>` | no | Intent topics. Accepts an Array of up to 50 Strings. See the 'Intent Topics' endpoint for values. Send multiple values as a array. |
| `signalStartDate` | body | `string` | no | Start date for a company signaling interest in a topic |
| `signalEndDate` | body | `string` | no | End date for a company signaling interest in a topic |
| `signalScoreMin` | body | `number` | no | Minimum signal score. Use with signalScoreMax to form a range. Minimum score is 60 and maximum is 100. |
| `signalScoreMax` | body | `number` | no | Maximum signal score. Use with signalScoreMin to form a range. Minimum score is 60 and maximum is 100. |
| `audienceStrengthMin` | body | `string` | no | Minimum audience strength score. Use with audienceStrengthMax to form a range. Values are A, B, C, D, and E, with A indicating a larger audience. |
| `audienceStrengthMax` | body | `string` | no | Maximum audience strength score. Use with audienceStrengthMin to form a range. Values are A, B, C, D, and E, with A indicating a larger audience. |
| `findRecommendedContacts` | body | `boolean` | no | Flag to indicate whether recommended contacts should be fetched in result or not. Default is true |
| `companyId` | body | `number` | no | Unique ZoomInfo identifier for a company |
| `companyName` | body | `string` | no | Company name |
| `companyWebsite` | body | `string` | no | The website of the company you are searching for |
| `sortBy` | body | `string` | no | Sorts results by valid output fields |
| `sortOrder` | body | `string` | no | Default value is desc. It accepts the following values { Asc, Ascending, desc, descending } |
