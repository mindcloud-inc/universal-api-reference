# List Mining Pools with Mempool

Retrieves mining pools from Mempool for a time period.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/mining/pools/[:time_period]`
- **Base URL:** `https://mempool.space/api`
- **Official documentation:** [List Mining Pools](https://mempool.space/docs/api/rest)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `time_period` | path | `string` | yes | Mining pool aggregation period, such as 1w, 1m, 3m, 6m, or 1y. |
