# Duplicate Event with Airmeet

Creates a duplicate event in Airmeet.

## Endpoint

- **Method:** `POST`
- **Path:** `/airmeet/{airmeetId}/duplication`
- **Base URL:** `https://api-gateway-prod.us.airmeet.com/prod`
- **Official documentation:** [Duplicate Event](https://help.airmeet.com/support/solutions/articles/82000909770-3-manage-event-airmeet-public-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `airmeetId` | path | `string` | yes | The source Airmeet event ID to duplicate. |
| `duplicateSpeakers` | body | `boolean` | no | Set true to include the original event speakers in the duplicate. |
| `eventName` | body | `string` | yes | Name for the duplicate event. |
| `startTime` | body | `number` | yes | Start time for the duplicate event as a Unix timestamp in milliseconds. |
| `timeZone` | body | `string` | yes | Canonical time zone name for the duplicate event. |
