# Get Datacenter Private Link with Astra

Retrieves private link details for an Astra datacenter.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/organizations/clusters/:databaseId/datacenters/:datacenterId/private-link`
- **Base URL:** `https://api.astra.datastax.com`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `databaseId` | path | `string` | yes | The Astra database ID. |
| `datacenterId` | path | `string` | yes | The Astra datacenter ID. |
