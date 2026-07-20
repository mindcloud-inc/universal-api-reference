# Get Mining Hashrate with Mempool

Retrieves network hashrate and difficulty from Mempool.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/mining/hashrate/[:time_period]`
- **Base URL:** `https://mempool.space/api`
- **Official documentation:** [Get Mining Hashrate](https://mempool.space/docs/api/rest)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `time_period` | path | `string` | yes | Hashrate aggregation period, such as 3d, 1w, 1m, 3m, 6m, or 1y. |
