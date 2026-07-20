# Get Usage Data With Paginated Groupings with Metronome

Retrieves paginated grouped usage data from Metronome.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/usage/groups`
- **Base URL:** `https://api.metronome.com`
- **Official documentation:** [Get Usage Data With Paginated Groupings](https://docs.metronome.com/api-reference/usage/get-usage-data-with-paginated-groupings)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customer_id` | body | `string` | yes | The customer ID. |
| `billable_metric_id` | body | `string` | yes | The billable metric ID. |
| `window_size` | body | `string` | yes | Aggregation window size. |
| `starting_on` | body | `string` | no | — |
| `ending_before` | body | `string` | no | — |
