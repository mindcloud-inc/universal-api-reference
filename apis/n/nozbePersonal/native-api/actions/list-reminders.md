# List Reminders with Nozbe Personal

Retrieves accessible reminders from Nozbe Personal.

## Endpoint

- **Method:** `GET`
- **Path:** `/reminders`
- **Base URL:** `https://api4.nozbe.com/v1/api`
- **Official documentation:** [List Reminders](https://api4.nozbe.com/v1/api#/reminders/getReminders)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `task_id` | query | `string` | no |
| `fields` | query | `string` | no |
| `sortBy` | query | `string` | no |
