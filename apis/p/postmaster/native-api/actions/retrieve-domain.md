# Retrieve Domain with Postmaster+

Retrieves domain details from the Postmaster+ API.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/domains/:id`
- **Base URL:** `https://postmasterplus.app`
- **Official documentation:** [Retrieve Domain](https://postmasterplus.app/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `end_date` | query | `string` | no | Filter related IPs until this date (Y-m-d). Maximum selected range is 90 days. |
| `id` | path | `string` | yes | The ULID of the domain. |
| `related_ips_page` | query | `number` | no | The page number for related IP results. |
| `start_date` | query | `string` | no | Filter related IPs from this date (Y-m-d). Maximum selected range is 90 days. |
