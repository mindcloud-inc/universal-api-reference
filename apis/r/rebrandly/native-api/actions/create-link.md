# Create Link with Rebrandly

Creates a new link in Rebrandly.

## Endpoint

- **Method:** `POST`
- **Path:** `/links`
- **Base URL:** `https://api.rebrandly.com/v1`
- **Official documentation:** [Create Link](https://developers.rebrandly.com/docs/create-a-new-link)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `destination` | body | `string` | yes | The URL that the branded short link should redirect to. |
| `slashtag` | body | `string` | no | Custom keyword portion of the branded short link. |
| `title` | body | `string` | no | Human-readable title for the branded short link. |
