# Delete Saved Search with Sourcegraph

Deletes a saved search from Sourcegraph.

## Endpoint

- **Method:** `POST`
- **Path:** `/.api/graphql`
- **Base URL:** `https://sourcegraph.com`
- **Official documentation:** [Delete Saved Search](https://sourcegraph.com/docs/api/graphql)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.id` | body | `string` | no | The Sourcegraph saved search ID to delete. |
