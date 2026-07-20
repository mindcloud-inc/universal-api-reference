# Download Job Results with NeverBounce

Retrieves downloadable job results from NeverBounce.

## Endpoint

- **Method:** `GET`
- **Path:** `/jobs/download`
- **Base URL:** `https://api.neverbounce.com/v4.2`
- **Official documentation:** [Download Job Results](https://developers.neverbounce.com/reference/jobs-download)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `job_id` | query | `number` | yes | NeverBounce job identifier. |
| `valids` | query | `boolean` | no | Include valid rows in the downloaded CSV. |
| `invalids` | query | `boolean` | no | Include invalid rows in the downloaded CSV. |
| `catchalls` | query | `boolean` | no | Include catchall rows in the downloaded CSV. |
| `unknowns` | query | `boolean` | no | Include unknown rows in the downloaded CSV. |
| `disposables` | query | `boolean` | no | Include disposable rows in the downloaded CSV. |
