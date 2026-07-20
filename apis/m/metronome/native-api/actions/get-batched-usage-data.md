# Get Batched Usage Data with Metronome

Retrieves batched usage data from Metronome.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/usage`
- **Base URL:** `https://api.metronome.com`
- **Official documentation:** [Get Batched Usage Data](https://docs.metronome.com/api-reference/usage/get-batched-usage-data)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `window_size` | body | `string` | yes | Aggregation window size. |
| `starting_on` | body | `string` | yes | Start of the usage window. |
| `ending_before` | body | `string` | yes | End of the usage window. |
