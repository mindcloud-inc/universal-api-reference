# List Activities with Nutshell

Retrieves activities from Nutshell.

## Endpoint

- **Method:** `GET`
- **Path:** `/activities`
- **Base URL:** `https://app.nutshell.com/rest`
- **Official documentation:** [List Activities](https://developers.nutshell.com/reference)

## Capabilities

This operation supports [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `q` | query | `string` | no | Search across activities. |
| `limit` | query | `date` | no | Maximum number of activities to return. |
| `filter[activityType][]` | query | `array<number>` | no | Filter activities by activity type. Send multiple values as a array. |
| `filter[status][]` | query | `array<string>` | no | Filter activities by status. Send multiple values as a array. |
| `filter[participant][]` | query | `array<string>` | no | Filter activities by participant. Send multiple values as a array. |
| `filter[flagged]` | query | `boolean` | no | Filter to flagged or unflagged activities. |
| `filter[isImportant]` | query | `boolean` | no | Filter to important or non-important activities. |
| `filter[leadPriority][]` | query | `string` | no | Filter activities by lead priority. |
| `filter[dateMin]` | query | `date` | no | Return activities on or after this date. |
| `filter[dateMax]` | query | `date` | no | Return activities on or before this date. |
