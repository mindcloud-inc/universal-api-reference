# Retrieve IP Feed with Postmaster+

Retrieves feed items for an IP in Postmaster+.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/ips/:id/feed`
- **Base URL:** `https://postmasterplus.app`
- **Official documentation:** [Retrieve IP Feed](https://postmasterplus.app/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `date` | query | `string` | no | Filter feed items reported on or after this date in Y-m-d format. |
| `id` | path | `string` | yes | The ULID of the IP. |
