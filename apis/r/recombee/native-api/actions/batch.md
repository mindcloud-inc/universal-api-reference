# Batch with Recombee

Creates a batch request in Recombee.

## Endpoint

- **Method:** `POST`
- **Path:** `/batch/`
- **Base URL:** `https://rapi.recombee.com/{databaseId}`
- **Official documentation:** [Batch](https://docs.recombee.com/api)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `distinctRecomms` | body | `string` | no |
| `requests` | body | `list<object>` | yes |
