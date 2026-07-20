# Create Batch Verification Job with ClearBounce

Creates a batch verification job in ClearBounce.

## Endpoint

- **Method:** `POST`
- **Path:** `/bulk/upload`
- **Base URL:** `https://api.clearbounce.net/api/v1`
- **Official documentation:** [Create Batch Verification Job](https://docs.clearbounce.net/api-reference/batch-verification)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `emails[]` | body | `array<string>` | yes | Array of email addresses to verify in one batch request. |
