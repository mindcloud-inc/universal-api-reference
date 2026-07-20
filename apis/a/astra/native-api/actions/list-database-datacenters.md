# List Database Datacenters with Astra

Retrieves datacenters for an Astra database.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/databases/:databaseId/datacenters`
- **Base URL:** `https://api.astra.datastax.com`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `all` | query | `boolean` | no | Include terminated datacenters when true. |
| `databaseId` | path | `string` | yes | The Astra database ID. |
