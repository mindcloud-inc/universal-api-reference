# Get Link Details with Linkbreakers

Retrieves detailed link information from Linkbreakers.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/links/:id`
- **Base URL:** `https://api.linkbreakers.com`
- **Official documentation:** [Get Link Details](https://linkbreakers.com/help/api/links)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The ID of the link to retrieve. |
| `include[]` | query | `array<string>` | no | Related resources to include in the response. |
