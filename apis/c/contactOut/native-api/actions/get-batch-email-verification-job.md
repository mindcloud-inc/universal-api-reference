# Get Batch Email Verification Job with ContactOut

Retrieves a batch email verification job from ContactOut.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/email/verify/batch/:job_uuid`
- **Base URL:** `https://api.contactout.com`
- **Official documentation:** [Get Batch Email Verification Job](https://api.contactout.com/#bulk)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `job_uuid` | path | `string` | yes | The bulk email verification job identifier. |
