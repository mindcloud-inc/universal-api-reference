# List Plans with Donorbox

Retrieves plans from Donorbox.

## Endpoint

- **Method:** `GET`
- **Path:** `/plans`
- **Base URL:** `https://donorbox.org/api/v1`
- **Official documentation:** [List Plans](https://github.com/donorbox/donorbox-api#plans)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | query | `list<string>` | no | Filter plans by donor email. |
| `first_name` | query | `string` | no | Filter plans by donor first name. |
| `last_name` | query | `string` | no | Filter plans by donor last name. |
| `campaign_id` | query | `list<string>` | no | Filter plans by campaign ID. |
| `campaign_name` | query | `string` | no | Filter plans by campaign name. |
| `donor_id` | query | `string` | no | Filter plans by donor ID. |
| `date_from` | query | `string` | no | Filter plans from date (YYYY-mm-dd). |
| `date_to` | query | `string` | no | Filter plans to date (YYYY-mm-dd). |
