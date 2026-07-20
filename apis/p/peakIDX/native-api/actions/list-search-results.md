# List Search Results with PeakIDX

Retrieves listings for a saved search in PeakIDX.

## Endpoint

- **Method:** `GET`
- **Path:** `https://{siteName}.peakidxsites.com/search-results-api/:searchEmbedId`
- **Base URL:** `https://account.peakidxsites.com`
- **Official documentation:** [List Search Results](https://docs.peakidx.com/api/search-results-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `searchEmbedId` | path | `string` | yes | The saved search embed identifier from the PeakIDX Search Embeds page. |
| `offset` | query | `number` | no | Starting position for the results. PeakIDX docs allow values from 0 through 10000. |
| `limit` | query | `number` | no | Maximum number of results to return. PeakIDX docs allow values from 0 through 200. |
