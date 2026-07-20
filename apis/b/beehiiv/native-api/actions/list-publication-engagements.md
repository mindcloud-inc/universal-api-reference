# List Publication Engagements with Beehiiv

Retrieves publication engagements from Beehiiv.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/publications/:publicationId/engagements`
- **Base URL:** `https://api.beehiiv.com`
- **Official documentation:** [List Publication Engagements](https://developers.beehiiv.com/api-reference/engagements/index)

## Capabilities

This operation supports [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `publicationId` | path | `string` | yes | The prefixed ID of the publication object. |
| `start_date` | query | `string` | no | The starting date in YYYY-MM-DD format. |
| `number_of_days` | query | `number` | no | Number of days to return metrics for (1-31). |
| `granularity` | query | `string` | no | Granularity for reported metrics. |
| `email_type` | query | `string` | no | Filter engagement by email type. |
| `direction` | query | `string` | no | Sort direction (asc or desc). |
