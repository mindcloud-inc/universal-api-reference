# Get User By Username with Sourcegraph

Retrieves a user from Sourcegraph by username.

## Endpoint

- **Method:** `POST`
- **Path:** `/.api/graphql`
- **Base URL:** `https://sourcegraph.com`
- **Official documentation:** [Get User By Username](https://sourcegraph.com/docs/api/graphql)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.username` | body | `string` | no | The Sourcegraph username to retrieve. |
