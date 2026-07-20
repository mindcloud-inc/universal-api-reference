# Update Saved Search with Sourcegraph

Updates a saved search in Sourcegraph.

## Endpoint

- **Method:** `POST`
- **Path:** `/.api/graphql`
- **Base URL:** `https://sourcegraph.com`
- **Official documentation:** [Update Saved Search](https://sourcegraph.com/docs/api/graphql)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.description` | body | `string` | no | The updated saved search description. |
| `variables.id` | body | `string` | no | The Sourcegraph saved search ID to update. |
| `variables.query` | body | `string` | no | The updated saved search query. Sourcegraph requires an explicit patternType filter in the query text. |
