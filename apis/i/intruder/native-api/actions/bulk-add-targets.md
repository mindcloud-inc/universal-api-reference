# Bulk Add Targets with Intruder

## Endpoint

- **Method:** `POST`
- **Path:** `/targets/bulk/`
- **Base URL:** `https://api.intruder.io/v1`
- **Official documentation:** [Bulk Add Targets](https://developers.intruder.io/reference/targets_bulk_create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `addresses[]` | body | `array<string>` | yes | Target addresses to bulk add. |
