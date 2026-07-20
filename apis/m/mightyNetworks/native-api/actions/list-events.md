# List Events with Mighty Networks

Retrieves events from a Mighty Networks network.

## Endpoint

- **Method:** `GET`
- **Path:** `/networks/:network_id/events`
- **Base URL:** `https://api.mn.co/admin/v1`
- **Official documentation:** [List Events](https://docs.mightynetworks.com/api-reference/events/returns-a-paginated-list-of-events-in-the-network)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `network_id` | path | `string` | yes | The Mighty Networks network ID or subdomain for the request path. |
