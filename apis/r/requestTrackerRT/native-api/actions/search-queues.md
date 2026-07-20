# Search Queues with Request Tracker (RT)

Finds queues in Request Tracker.

## Endpoint

- **Method:** `GET`
- **Path:** `queues`
- **Base URL:** `https://try.requesttracker.io/sufongepl_57381/REST/2.0/`
- **Official documentation:** [Search Queues](https://docs.bestpractical.com/rt/6.0.2/RT/REST2.html#Queues)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fields` | query | `string` | no | Comma-separated RT fields to include in each queue result. |
| `query` | query | `string` | yes | JSON search array for RT queues, serialized as a string. |
