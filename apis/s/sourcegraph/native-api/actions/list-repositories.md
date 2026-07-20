# List Repositories with Sourcegraph

Retrieves repositories from Sourcegraph.

## Endpoint

- **Method:** `POST`
- **Path:** `/.api/graphql`
- **Base URL:** `https://sourcegraph.com`
- **Official documentation:** [List Repositories](https://sourcegraph.com/docs/api/graphql)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.query` | body | `string` | no | Optional repository search query text. |
| `variables.first` | body | `number` | no | Maximum number of repositories to return. |
