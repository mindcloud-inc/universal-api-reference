# List Time Entries with Teamdeck

Retrieves time entries from your Teamdeck organization.

## Endpoint

- **Method:** `GET`
- **Path:** `/time-entries`
- **Base URL:** `https://api.teamdeck.io/v1`
- **Official documentation:** [List Time Entries](https://teamdeck.io/developers/api#operation/timeEntriesList)

## Capabilities

This operation supports [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `fields` | query | `string` | no |
| `expand` | query | `string` | no |
| `resource_id` | query | `string` | no |
| `project_id` | query | `string` | no |
| `external_id` | query | `string` | no |
| `start_date_from` | query | `string` | no |
| `start_date_to` | query | `string` | no |
| `end_date_from` | query | `string` | no |
| `end_date_to` | query | `string` | no |
| `date` | query | `string` | no |
