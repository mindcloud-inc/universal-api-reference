# Search Assets with NASA Image and Video Library

Finds assets in NASA Image and Video Library by search criteria.

## Endpoint

- **Method:** `GET`
- **Path:** `/search`
- **Base URL:** `https://images-api.nasa.gov`
- **Official documentation:** [Search Assets](https://images.nasa.gov/docs/images.nasa.gov_api_docs.pdf)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `q` | query | `string` | no | Free text terms to match across indexed NASA media metadata. Provide at least one search parameter somewhere in this action. |
| `nasa_id` | query | `string` | no | Restrict results to a specific NASA media asset ID. |
| `media_type` | query | `string` | no | Comma-separated media types to return. Available values: image, video, audio. |
| `title` | query | `string` | no | Terms to search within asset titles. |
| `description` | query | `string` | no | Terms to search within asset descriptions. |
| `keywords` | query | `string` | no | Comma-separated keywords to search within asset keyword metadata. |
| `center` | query | `string` | no | Restrict results to a specific NASA center code such as JSC, KSC, or HQ. |
| `location` | query | `string` | no | Terms to search within asset location metadata. |
| `photographer` | query | `string` | no | Restrict results by the primary photographer name. |
| `year_start` | query | `string` | no | Restrict results to assets created on or after this year. Format: YYYY. |
| `year_end` | query | `string` | no | Restrict results to assets created on or before this year. Format: YYYY. |
| `page` | query | `number` | no | Page number to retrieve. Starts at 1. |
| `page_size` | query | `number` | no | Number of results per page. NASA documents a default of 100. |
| `description_508` | query | `string` | no | Terms to search within accessibility 508 descriptions. |
| `secondary_creator` | query | `string` | no | Restrict results by a secondary photographer or videographer name. |
