# List Saved Searches with Sourcegraph

Retrieves saved searches from Sourcegraph.

## Endpoint

- **Method:** `POST`
- **Path:** `/.api/graphql`
- **Base URL:** `https://sourcegraph.com`
- **Official documentation:** [List Saved Searches](https://sourcegraph.com/docs/api/graphql)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.first` | body | `number` | no | Maximum number of saved searches to return. |
