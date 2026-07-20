# List Activities with Runrun.it

Retrieves activities from Runrun.it.

## Endpoint

- **Method:** `GET`
- **Path:** `/activities`
- **Base URL:** `https://runrun.it/api/v1.0`
- **Official documentation:** [List Activities](https://runrun.it/api/documentation#activities-get-activities)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sort` | query | `string` | no | Sort by column |
| `sort_dir` | query | `string` | no | Sort direction ('asc' or 'desc') |
