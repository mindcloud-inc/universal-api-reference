# Batch Lookup Calls with CallScaler

Finds calls in CallScaler by batch lookup.

## Endpoint

- **Method:** `POST`
- **Path:** `/calls/batch`
- **Base URL:** `https://callscaler.com/api/v1`
- **Official documentation:** [Batch Lookup Calls](https://callscaler.com/docs/api-calls)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ids[]` | body | `array<string>` | yes | Up to 100 call IDs to retrieve. Send multiple values as a array. |
