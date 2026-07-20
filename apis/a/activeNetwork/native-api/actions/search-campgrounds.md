# Search Campgrounds with Active Network

Finds campgrounds in Active Network.

## Endpoint

- **Method:** `GET`
- **Path:** `/camping/campgrounds/`
- **Base URL:** `http://api.amp.active.com`
- **Official documentation:** [Search Campgrounds](https://developer.active.com/docs/read/Campground_Search_API)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `amenity` | query | `number` | no | Campground amenity code such as fishing, hiking, or golf. |
| `eqplen` | query | `number` | no | Required equipment length for the campsite. |
| `hookup` | query | `string` | no | Electric hookup code. |
| `landmarkLat` | query | `string` | no | Latitude for fixed-point campground searches. |
| `landmarkLong` | query | `string` | no | Longitude for fixed-point campground searches. |
| `landmarkName` | query | `string` | no | Name label required with landmark latitude and longitude. |
| `Maxpeople` | query | `string` | no | Maximum number of campers the site must support. |
| `pets` | query | `string` | no | Pets-allowed code. |
| `pname` | query | `string` | no | Return campgrounds whose names contain this text. |
| `pstate` | query | `string` | no | Two-character US state or Canadian province code. |
| `pull` | query | `string` | no | Pull-through driveway code. |
| `sewer` | query | `string` | no | Sewer hookup code. |
| `siteType` | query | `number` | no | Site type code such as RV, tent, trailer, or cabin. |
| `water` | query | `string` | no | Water hookup code. |
| `waterfront` | query | `string` | no | Waterfront-site code. |
