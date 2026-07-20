# Get Weld Data with Anvil

Retrieves a single weld data record from Anvil.

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `https://graphql.useanvil.com`
- **Official documentation:** [Get Weld Data](https://www.useanvil.com/docs/api/graphql/reference/#query-weldData)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.eid` | body | `string` | yes | Provide EID for Get Weld Data. |
