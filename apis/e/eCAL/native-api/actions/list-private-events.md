# List Private Events with ECAL

Retrieves a subscriber's private events from ECAL.

## Endpoint

- **Method:** `GET`
- **Path:** `/event/`
- **Base URL:** `https://api.ecal.com/apiv2`
- **Official documentation:** [List Private Events](https://docs.ecal.com/reference/private/single.html#get-private-events)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ecal_id` | query | `string` | yes | Subscriber ecal_id value for private events. |
