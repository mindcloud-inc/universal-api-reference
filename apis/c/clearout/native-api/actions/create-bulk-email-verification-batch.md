# Create Bulk Email Verification Batch with Clearout

Creates a bulk email verification batch in Clearout.

## Endpoint

- **Method:** `POST`
- **Path:** `/email_verify/bulk`
- **Base URL:** `https://api.clearout.io/v2`
- **Official documentation:** [Create Bulk Email Verification Batch](https://docs.clearout.io/developers/api/email-verify)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file` | body | `string` | yes | — |
| `optimize` | body | `string` | no | Can be either 'highest_accuracy' or 'fastest_turnaround' |
| `ignore_duplicate_file` | body | `string` | no | Whether to allow file with the same name and size that match with your recent upload |
