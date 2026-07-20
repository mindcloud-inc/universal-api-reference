# List Campaigns with Emelia

Retrieves campaign listings from Emelia.

## Endpoint

- **Method:** `POST`
- **Path:** `/graphql`
- **Base URL:** `https://graphql.emelia.io`
- **Official documentation:** [List Campaigns](https://docs-old.emelia.io/#operation-get_campaigns-post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `options` | body | `string` | no | Filter/options JSON for the campaign list query. Provide a JSON object string, for example {"status":"running"}. |
