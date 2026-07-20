# Create Activity with timeBuzzer

## Endpoint

- **Method:** `POST`
- **Path:** `/open-api/activities`
- **Base URL:** `https://my.timebuzzer.com`
- **Official documentation:** [Create Activity](https://my.timebuzzer.com/doc/#api-Activities-CreateActivity)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tiles[]` | body | `array<number>` | yes | Tile IDs to associate with the activity. |
| `startDate` | body | `string` | yes | Activity start timestamp in ISO 8601 format. |
| `endDate` | body | `string` | yes | Activity end timestamp in ISO 8601 format. |
| `startUtcOffset` | body | `string` | yes | UTC offset at the activity start time. |
| `endUtcOffset` | body | `string` | yes | UTC offset at the activity end time. |
| `note` | body | `string` | no | Optional note for the activity. |
| `userId` | body | `number` | yes | User ID that owns the activity. |
