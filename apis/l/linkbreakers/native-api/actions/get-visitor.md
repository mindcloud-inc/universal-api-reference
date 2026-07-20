# Get a Visitor with Linkbreakers

Retrieves detailed visitor information from Linkbreakers.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/visitors/:id`
- **Base URL:** `https://api.linkbreakers.com`
- **Official documentation:** [Get a Visitor](https://linkbreakers.com/help/api/visitors)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The ID of the visitor to retrieve. |
| `include[]` | query | `array<string>` | no | Relationships to include in the visitor response. |
