# Update a campaign by its ID with Kite Suite

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v1/campaign/:id`
- **Base URL:** `https://api.kitesuite.com`
- **Official documentation:** [Update a campaign by its ID](https://api.kitesuite.com/swagger/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The ID of the campaign to update. |
| `body` | body | `object` | yes | Request body |
| `name` | body | `string` | yes | The name of the campaign. |
| `status` | body | `string` | yes | The status of the campaign (e.g., "resume", "pause"). |
| `options` | body | `object` | yes | Additional campaign options. |
| `start` | body | `string` | yes | The start date of the campaign. |
| `end` | body | `string` | yes | The end date of the campaign. |
