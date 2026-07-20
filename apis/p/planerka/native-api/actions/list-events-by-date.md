# List events by date with Planerka

Retrieves events from Planerka for a specific date.

## Endpoint

- **Method:** `GET`
- **Path:** `/event/`
- **Base URL:** `https://planerka.app/rest/v1`
- **Official documentation:** [List events by date](https://planerka.app/rest/doc)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `date` | query | `string` | no | Date in d.m.Y format used to list events for a single day. |
