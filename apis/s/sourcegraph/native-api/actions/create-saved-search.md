# Create Saved Search with Sourcegraph

Creates a saved search in Sourcegraph.

## Endpoint

- **Method:** `POST`
- **Path:** `/.api/graphql`
- **Base URL:** `https://sourcegraph.com`
- **Official documentation:** [Create Saved Search](https://sourcegraph.com/docs/api/graphql)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.description` | body | `string` | no | The saved search description. |
| `variables.owner` | body | `string` | no | The Sourcegraph user ID that will own the saved search. |
| `variables.query` | body | `string` | no | The saved search query. Sourcegraph requires an explicit patternType filter in the query text. |
