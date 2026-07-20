# Get Campground Details with Active Network

Retrieves campground details in Active Network.

## Endpoint

- **Method:** `GET`
- **Path:** `/camping/campground/details`
- **Base URL:** `http://api.amp.active.com`
- **Official documentation:** [Get Campground Details](https://developer.active.com/docs/read/Campground_Details_API)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contractCode` | query | `string` | yes | Jurisdiction code returned by campground search. |
| `parkId` | query | `number` | yes | Unique campground facility ID returned by campground search. |
