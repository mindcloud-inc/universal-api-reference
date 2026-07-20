# List System-Wide Charges with Cerbo

Retrieves system-wide charges from Cerbo.

## Endpoint

- **Method:** `GET`
- **Path:** `/charges`
- **Base URL:** `https://{tenant}.md-hq.com/api/v1`
- **Official documentation:** [List System-Wide Charges](https://docs.cer.bo/#tag/Charges/operation/listAllCharges)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `date_method` | query | `string` | no | If filtering by date range, should the range be calculated by date the charge was created, or the recorded transaction date? Valid arguments are 'created' and 'transaction' (created is the default). |
| `start_date` | query | `date` | no | Show charges from after this date (calculated by date_method). |
| `end_date` | query | `date` | no | Show charges from before this date (calculated by date_method). |
