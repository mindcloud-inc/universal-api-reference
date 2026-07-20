# Launch Scrap with Emelia

Creates a scrap in Emelia from a Sales Navigator URL.

## Endpoint

- **Method:** `POST`
- **Path:** `/graphql`
- **Base URL:** `https://graphql.emelia.io`
- **Official documentation:** [Launch Scrap](https://docs-old.emelia.io/#operation-launch_a_scrap-post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `authes` | body | `string` | yes | Credential ID list. Provide a JSON array string, for example ["cred_id"]. |
| `name` | body | `string` | yes | Scrap name |
| `plannedStart` | body | `string` | no | Optional planned start datetime string |
| `url` | body | `string` | yes | Source URL |
