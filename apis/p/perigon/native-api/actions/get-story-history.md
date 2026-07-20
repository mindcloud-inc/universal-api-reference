# Get Story History with Perigon

Retrieves historical changes for Perigon stories over time.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/stories/history`
- **Base URL:** `https://api.perigon.io/v1`
- **Official documentation:** [Get Story History](https://docs.perigon.io/docs/stories-overview)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `clusterId` | query | `string` | no | Send multiple values as a string separated by `,`. |
| `from` | query | `date` | no | — |
| `to` | query | `date` | no | — |
| `sortBy` | query | `string` | no | — |
| `page` | query | `number` | no | — |
| `size` | query | `number` | no | — |
| `changelogExists` | query | `boolean` | no | — |
