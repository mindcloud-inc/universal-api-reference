# Search Campsites with Active Network

Finds campsites in Active Network.

## Endpoint

- **Method:** `GET`
- **Path:** `/camping/campsites/`
- **Base URL:** `http://api.amp.active.com`
- **Official documentation:** [Search Campsites](https://developer.active.com/docs/read/Campsite_Search_API)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contractCode` | query | `string` | yes | Jurisdiction code returned by campground search. |
| `eqplen` | query | `number` | no | Required equipment length for the campsite. |
| `hookup` | query | `string` | no | Electric hookup code. |
| `Maxpeople` | query | `string` | no | Maximum number of campers the site must support. |
| `parkId` | query | `number` | yes | Unique campground facility ID returned by campground search. |
| `pets` | query | `string` | no | Pets-allowed code. |
| `pull` | query | `string` | no | Pull-through driveway code. |
| `sewer` | query | `string` | no | Sewer hookup code. |
| `siteType` | query | `number` | no | Site type code such as RV, tent, trailer, or cabin. |
| `water` | query | `string` | no | Water hookup code. |
| `waterfront` | query | `string` | no | Waterfront-site code. |
