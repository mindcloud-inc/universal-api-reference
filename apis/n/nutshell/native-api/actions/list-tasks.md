# List Tasks with Nutshell

Retrieves tasks from Nutshell.

## Endpoint

- **Method:** `GET`
- **Path:** `/tasks`
- **Base URL:** `https://app.nutshell.com/rest`
- **Official documentation:** [List Tasks](https://developers.nutshell.com/reference)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `q` | query | `string` | no | Search across tasks. |
| `filter[assignee][]` | query | `array<string>` | no | Filter tasks by assignee. Send multiple values as a array. |
| `filter[relatedEntity]` | query | `string` | no | Filter tasks by the related entity. |
| `filter[dateMin]` | query | `date` | no | Return tasks on or after this date. |
| `filter[dateMax]` | query | `date` | no | Return tasks on or before this date. |
