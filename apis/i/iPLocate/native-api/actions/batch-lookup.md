# Batch Lookup with IPLocate

## Endpoint

- **Method:** `POST`
- **Path:** `/batch`
- **Base URL:** `https://iplocate.io/api`
- **Official documentation:** [Batch Lookup](https://www.iplocate.io/docs/ip-intelligence-api/batch-lookup)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ips[]` | body | `array<string>` | yes | Array of IPv4 or IPv6 addresses to look up in one request. IPLocate allows between 1 and 1000 items per batch. |
