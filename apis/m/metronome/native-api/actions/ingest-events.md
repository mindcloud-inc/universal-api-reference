# Ingest Events with Metronome

Ingests events into Metronome.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/ingest`
- **Base URL:** `https://api.metronome.com`
- **Official documentation:** [Ingest Events](https://docs.metronome.com/api-reference/usage/ingest-events)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `events[]` | body | `array<object>` | yes |
