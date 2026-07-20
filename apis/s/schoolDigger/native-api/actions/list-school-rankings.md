# List School Rankings with SchoolDigger

Retrieves school rankings from SchoolDigger.

## Endpoint

- **Method:** `GET`
- **Path:** `/rankings/schools/:st`
- **Base URL:** `https://api.schooldigger.com/v2.3`
- **Official documentation:** [List School Rankings](https://developer.schooldigger.com/llms-full.txt)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `st` | path | `string` | yes | Two-letter state code for the ranking list. |
| `year` | query | `number` | no | Ranking year. Defaults to the most recent year when omitted. |
| `level` | query | `list` | no | Ranking level: Elementary, Middle, or High. Accepted values: `0`, `1`, `2`. |
