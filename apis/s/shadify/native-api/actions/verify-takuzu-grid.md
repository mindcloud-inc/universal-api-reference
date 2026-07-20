# Verify Takuzu Grid with Shadify

Retrieves a Takuzu validation result from Shadify.

## Endpoint

- **Method:** `POST`
- **Path:** `/takuzu/verifier`
- **Base URL:** `https://shadify.yurace.pro/api`
- **Official documentation:** [Verify Takuzu Grid](https://shadify.yurace.pro/modules/takuzu.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `task[]` | body | `array<array>` | yes | Required Takuzu grid as a square array of 0 and 1 strings. |
