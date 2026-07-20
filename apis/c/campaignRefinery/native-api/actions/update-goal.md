# Update Goal with Campaign Refinery

Updates an existing goal in Campaign Refinery.

## Endpoint

- **Method:** `POST`
- **Path:** `/goals/update-goal`
- **Base URL:** `https://app.campaignrefinery.com/rest`
- **Official documentation:** [Update Goal](https://developers.campaignrefinery.com/reference/update-goal)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `string` | yes | The goal UUID. |
| `name` | body | `string` | no | The goal's name. |
