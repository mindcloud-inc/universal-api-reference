# Get Organization By Name with Sourcegraph

Retrieves an organization from Sourcegraph by name.

## Endpoint

- **Method:** `POST`
- **Path:** `/.api/graphql`
- **Base URL:** `https://sourcegraph.com`
- **Official documentation:** [Get Organization By Name](https://sourcegraph.com/docs/api/graphql)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.name` | body | `string` | no | The Sourcegraph organization name to retrieve. |
