# Create Search Context with Sourcegraph

Creates a search context in Sourcegraph.

## Endpoint

- **Method:** `POST`
- **Path:** `/.api/graphql`
- **Base URL:** `https://sourcegraph.com`
- **Official documentation:** [Create Search Context](https://sourcegraph.com/docs/api/graphql)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.description` | body | `string` | no | The search context description. |
| `variables.name` | body | `string` | no | The search context name. |
| `variables.namespace` | body | `string` | no | The Sourcegraph namespace ID that will own the search context. |
| `variables.query` | body | `string` | no | The repository filter query for the search context. |
