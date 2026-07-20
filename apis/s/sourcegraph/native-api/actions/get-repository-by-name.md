# Get Repository By Name with Sourcegraph

Retrieves a repository from Sourcegraph by name.

## Endpoint

- **Method:** `POST`
- **Path:** `/.api/graphql`
- **Base URL:** `https://sourcegraph.com`
- **Official documentation:** [Get Repository By Name](https://sourcegraph.com/docs/api/graphql)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.name` | body | `string` | no | The full Sourcegraph repository name, such as github.com/org/repo. |
