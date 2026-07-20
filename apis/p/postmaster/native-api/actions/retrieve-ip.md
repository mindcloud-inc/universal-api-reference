# Retrieve IP with Postmaster+

Retrieves IP details from the Postmaster+ API.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/ips/:id`
- **Base URL:** `https://postmasterplus.app`
- **Official documentation:** [Retrieve IP](https://postmasterplus.app/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `end_date` | query | `string` | no | Filter related domains until this date (Y-m-d). Maximum selected range is 90 days. |
| `id` | path | `string` | yes | The ULID of the IP. |
| `related_domains_page` | query | `number` | no | The page number for related domain results. |
| `start_date` | query | `string` | no | Filter related domains from this date (Y-m-d). Maximum selected range is 90 days. |
