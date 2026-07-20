# Get Batch Verification Results with MailFloss

Retrieves batch email verification results from MailFloss.

## Endpoint

- **Method:** `GET`
- **Path:** `/batch-verify/:id/results`
- **Base URL:** `https://api.mailfloss.com`
- **Official documentation:** [Get Batch Verification Results](https://developers.mailfloss.com/9bbG-reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Batch verification job ID. |
| `next` | query | `number` | yes | Next page of results to fetch. |
| `per_page` | query | `number` | no | Number of results to return per page. Max 1000; defaults to 100. |
