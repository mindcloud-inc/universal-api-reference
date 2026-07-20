# Update Form with Campaign Refinery

Updates an existing form in Campaign Refinery.

## Endpoint

- **Method:** `POST`
- **Path:** `/forms/update-form`
- **Base URL:** `https://app.campaignrefinery.com/rest`
- **Official documentation:** [Update Form](https://developers.campaignrefinery.com/reference/update-form)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `string` | yes | The form UUID. |
| `name` | body | `string` | no | The form's name. |
