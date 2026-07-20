# Get Viewer with Universe

Retrieves the authenticated viewer from Universe.

## Endpoint

- **Method:** `POST`
- **Path:** `/graphql`
- **Base URL:** `https://www.universe.com`
- **Official documentation:** [Get Viewer](https://developers.universe.com/docs/basic-usage-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | body | `string` | yes | Default read-only viewer query used to validate the authenticated Universe connection and inspect memberships. |
| `variables` | body | `object` | no | Optional GraphQL variables as a JSON object string for the default viewer query. |
