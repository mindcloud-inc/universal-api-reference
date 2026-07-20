# Update Activity with timeBuzzer

## Endpoint

- **Method:** `PUT`
- **Path:** `/open-api/activities/:id`
- **Base URL:** `https://my.timebuzzer.com`
- **Official documentation:** [Update Activity](https://my.timebuzzer.com/doc/#api-Activities-EditActivity)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The activity ID. |
| `tiles[]` | body | `array<number>` | yes | The tile IDs assigned to the activity. Send multiple values as a array. |
| `startDate` | body | `string` | yes | The activity start timestamp in ISO 8601 format. |
| `endDate` | body | `string` | yes | The activity end timestamp in ISO 8601 format. |
| `startUtcOffset` | body | `string` | yes | The UTC offset at the start of the activity. |
| `endUtcOffset` | body | `string` | yes | The UTC offset at the end of the activity. |
| `note` | body | `string` | no | The activity note. |
| `billed` | body | `boolean` | yes | Whether the activity is billed. |
| `userId` | body | `number` | yes | The user ID that owns the activity. |
