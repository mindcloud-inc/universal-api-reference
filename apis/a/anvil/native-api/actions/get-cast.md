# Get Cast with Anvil

Retrieves a single cast from Anvil.

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `https://graphql.useanvil.com`
- **Official documentation:** [Get Cast](https://www.useanvil.com/docs/api/graphql/reference/#query-cast)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.eid` | body | `string` | no | Provide EID for Get Cast. |
| `variables.versionNumber` | body | `number` | no | Provide Version Number for Get Cast. |
