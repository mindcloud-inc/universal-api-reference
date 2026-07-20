# Batch Transact Steps with Instant

Applies transaction steps to Instant records.

## Endpoint

- **Method:** `POST`
- **Path:** `/admin/transact`
- **Base URL:** `https://api.instantdb.com`
- **Official documentation:** [Batch Transact Steps](https://www.instantdb.com/docs/http-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `steps[]` | body | `array<array>` | yes | Transaction step array to send to Instant. |
