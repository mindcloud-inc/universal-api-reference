# List Hardware with Minerstat

Retrieves mining hardware from the Minerstat catalog.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/hardware`
- **Base URL:** `https://api.minerstat.com`
- **Official documentation:** [List Hardware](https://api.minerstat.com/docs-hardware/documentation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `type` | query | `string` | no | Hardware category like gpu or asic. |
| `brand` | query | `string` | no | Manufacturer or marketplace like antminer. |
