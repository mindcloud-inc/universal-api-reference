# List Events with Hipsy

Retrieves events from a Hipsy organisation.

## Endpoint

- **Method:** `GET`
- **Path:** `/organisation/:organisationSlug/events`
- **Base URL:** `https://api.hipsy.nl/v1`
- **Official documentation:** [List Events](https://docs.hipsy.nl/api-reference/list-events)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organisationSlug` | path | `string` | yes | Slug of the organisation whose events should be listed. |
| `period` | query | `list` | no | Which events to return: upcoming, past, or all. Accepted values: `all`, `past`, `upcoming`. |
