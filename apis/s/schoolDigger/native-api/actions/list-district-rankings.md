# List District Rankings with SchoolDigger

Retrieves district rankings from SchoolDigger.

## Endpoint

- **Method:** `GET`
- **Path:** `/rankings/districts/:st`
- **Base URL:** `https://api.schooldigger.com/v2.3`
- **Official documentation:** [List District Rankings](https://developer.schooldigger.com/llms-full.txt)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `st` | path | `string` | yes | Two-letter state code for the ranking list. |
| `year` | query | `number` | no | Ranking year. Defaults to the most recent year when omitted. |
