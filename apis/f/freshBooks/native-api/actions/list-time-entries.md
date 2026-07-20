# List Time Entries with FreshBooks

Retrieves time entries from FreshBooks for a business.

## Endpoint

- **Method:** `GET`
- **Path:** `/timetracking/business/:businessId/time_entries`
- **Base URL:** `https://api.freshbooks.com`
- **Official documentation:** [List Time Entries](https://www.freshbooks.com/api/time_entries)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `businessId` | path | `string` | yes | FreshBooks business ID. |
