# Enrich Scoops with Zoominfo

Enriches company scoops with ZoomInfo data.

## Endpoint

- **Method:** `POST`
- **Path:** `enrich/scoop`
- **Base URL:** `https://api.zoominfo.com/`
- **Official documentation:** [Enrich Scoops](https://api-docs.zoominfo.com/#545c603a-fbe5-48b6-b4b4-bdca626fead0)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `companyId` | body | `string` | no | ZoomInfo unique identifier for the company. Will accept a comma-separated list. |
| `companyName` | body | `string` | no | Company name. Accepts a pipe ('\|')-separated list. |
| `companyWebsite` | body | `string` | no | Company domain. Accepts a comma-separated list. |
| `publishedStartDate` | body | `string` | no | Starting date to search for scoops based on when published. Form a range using publishedEndDate or omit publishedEndDate to search to the current date. Uses YYYY-MM-DD format. |
| `publishedEndDate` | body | `string` | no | Ending date to search for scoops based on when published. Form a range using publishedEndDate. Uses YYYY-MM-DD format. |
| `updatedSinceCreation` | body | `boolean` | no | Include scoops that have been updated since publishedStartDate |
| `scoopType` | body | `string` | no | Retrieve scoops based on type (e.g. earnings, awards and partnerships). Accepts a comma-separated list of IDs from the endpoint: /lookup/scooptype. |
| `scoopTopic` | body | `string` | no | Retrieve scoops based on topic (e.g. integration, consolidation and compliance). Accepts a comma-separated list of IDs from the endpoint: /lookup/scooptopic. |
| `department` | body | `string` | no | Retrieve scoops based on department (e.g. IT, finance and HR). Accepts a comma-separated list of IDs from the endpoint: /lookup/scoopdepartment. |
| `scoopId` | body | `string` | no | ZoomInfo unique identifier for a scoop. Accepts a comma-separated list. |
| `description` | body | `string` | no | Search for scoops based on description.  Accepts a space-separated list of individual words. |
| `sortBy` | body | `string` | no | Sorts results by valid output fields |
| `sortOrder` | body | `string` | no | Default value is desc. It accepts the following values { asc, ascending, desc, descending |
