# Update Tag with Campaign Refinery

Updates an existing tag in Campaign Refinery.

## Endpoint

- **Method:** `POST`
- **Path:** `/tags/update-tag`
- **Base URL:** `https://app.campaignrefinery.com/rest`
- **Official documentation:** [Update Tag](https://developers.campaignrefinery.com/reference/update-tag)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `string` | yes | The tag UUID. |
| `name` | body | `string` | no | The tag's name. |
