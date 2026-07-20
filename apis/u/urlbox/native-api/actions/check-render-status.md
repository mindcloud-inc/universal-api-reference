# Check Render Status with Urlbox

Retrieves the status of a render from Urlbox.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/render/:renderId`
- **Base URL:** `https://api.urlbox.com`
- **Official documentation:** [Check Render Status](https://urlbox.com/docs/api#check-the-status-of-a-render)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `renderId` | path | `string` | yes | The render ID returned by the async render action |
