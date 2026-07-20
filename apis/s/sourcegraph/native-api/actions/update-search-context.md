# Update Search Context with Sourcegraph

Updates a search context in Sourcegraph.

## Endpoint

- **Method:** `POST`
- **Path:** `/.api/graphql`
- **Base URL:** `https://sourcegraph.com`
- **Official documentation:** [Update Search Context](https://sourcegraph.com/docs/api/graphql)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.description` | body | `string` | no | The updated search context description. |
| `variables.id` | body | `string` | no | The current Sourcegraph search context ID to update. If you rename a context, use the updated ID from the mutation response for future operations. |
| `variables.name` | body | `string` | no | The updated search context name. |
| `variables.query` | body | `string` | no | The updated repository filter query for the search context. |
