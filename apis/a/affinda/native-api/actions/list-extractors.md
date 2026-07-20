# Get list of all extractors with Affinda

Retrieves all accessible extractors from Affinda.

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/extractors`
- **Base URL:** `https://api.us1.affinda.com`
- **Official documentation:** [Get list of all extractors](https://docs.affinda.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `include_public_extractors` | query | `string` | no | Whether to include Affinda's off-the-shelf extractors. |
| `name` | query | `string` | no | Filter by name. |
| `organization` | query | `string` | yes | Filter by organization. |
| `validatable` | query | `string` | no | Filter by validatable. |
