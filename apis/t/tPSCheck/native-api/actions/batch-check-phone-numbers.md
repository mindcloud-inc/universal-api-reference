# Batch check phone numbers with TPSCheck

## Endpoint

- **Method:** `POST`
- **Path:** `/batch`
- **Base URL:** `https://api.tpscheck.uk`
- **Official documentation:** [Batch check phone numbers](https://www.tpscheck.uk/documentation/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `phones[]` | body | `array<string>` | yes | Array of UK phone numbers to verify. TPSCheck documents a maximum of 100 numbers per request on this endpoint. |
