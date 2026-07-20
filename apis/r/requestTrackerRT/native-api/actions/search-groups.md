# Search Groups with Request Tracker (RT)

Finds groups in Request Tracker.

## Endpoint

- **Method:** `GET`
- **Path:** `groups`
- **Base URL:** `https://try.requesttracker.io/sufongepl_57381/REST/2.0/`
- **Official documentation:** [Search Groups](https://docs.bestpractical.com/rt/6.0.2/RT/REST2.html#Groups)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fields` | query | `string` | no | Comma-separated RT fields to include in each group result. |
| `query` | query | `string` | yes | JSON search array for RT groups, serialized as a string. |
