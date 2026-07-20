# Verify Kuromasu Puzzle with Shadify

Retrieves a Kuromasu validation result from Shadify.

## Endpoint

- **Method:** `POST`
- **Path:** `/kuromasu/verifier`
- **Base URL:** `https://shadify.yurace.pro/api`
- **Official documentation:** [Verify Kuromasu Puzzle](https://shadify.yurace.pro/modules/kuromasu.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `solution[]` | body | `array<array>` | yes | Required completed Kuromasu grid. |
