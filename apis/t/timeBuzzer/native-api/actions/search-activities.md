# Search Activities with timeBuzzer

## Endpoint

- **Method:** `POST`
- **Path:** `/open-api/activities/filters`
- **Base URL:** `https://my.timebuzzer.com`
- **Official documentation:** [Search Activities](https://my.timebuzzer.com/doc/#api-Activities-GetFilteredActivities)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userIds[]` | body | `array<number>` | no | Optional user IDs to include. Send multiple values as a array. |
| `startDate` | body | `string` | no | The inclusive start timestamp in ISO 8601 format. |
| `endDate` | body | `string` | no | The inclusive end timestamp in ISO 8601 format. |
| `strictDate` | body | `boolean` | no | Whether the date boundaries should be strict. |
