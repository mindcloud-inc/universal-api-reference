# Create Bulk Email Finder Batch with Clearout

Creates a bulk email finder batch in Clearout.

## Endpoint

- **Method:** `POST`
- **Path:** `/email_finder/bulk`
- **Base URL:** `https://api.clearout.io/v2`
- **Official documentation:** [Create Bulk Email Finder Batch](https://docs.clearout.io/developers/api/email-finder)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file` | body | `string` | yes | — |
| `ignore_duplicate_file` | body | `string` | no | Whether to allow file with the same name and size that match with your recent upload |
