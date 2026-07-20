# Get Namespace By Name with Sourcegraph

Retrieves a namespace from Sourcegraph by name.

## Endpoint

- **Method:** `POST`
- **Path:** `/.api/graphql`
- **Base URL:** `https://sourcegraph.com`
- **Official documentation:** [Get Namespace By Name](https://sourcegraph.com/docs/api/graphql)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.name` | body | `string` | no | The Sourcegraph namespace name to resolve. |
