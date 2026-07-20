# Retrieve Domain Feed with Postmaster+

Retrieves feed items for a domain in Postmaster+.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/domains/:id/feed`
- **Base URL:** `https://postmasterplus.app`
- **Official documentation:** [Retrieve Domain Feed](https://postmasterplus.app/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `date` | query | `string` | no | Filter feed items reported on or after this date in Y-m-d format. |
| `id` | path | `string` | yes | The ULID of the domain. |
