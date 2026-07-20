# Publish Cast with Anvil

Publishes an existing cast in Anvil.

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `https://graphql.useanvil.com`
- **Official documentation:** [Publish Cast](https://www.useanvil.com/docs/api/graphql/reference/#mutation-publishCast)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.eid` | body | `string` | yes | Provide EID for Publish Cast. |
| `variables.title` | body | `string` | yes | Provide Title for Publish Cast. |
| `variables.description` | body | `string` | no | Provide Description for Publish Cast. |
