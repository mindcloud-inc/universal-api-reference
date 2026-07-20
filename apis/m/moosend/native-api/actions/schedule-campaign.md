# Schedule Campaign with Moosend

Schedules a campaign in Moosend.

## Endpoint

- **Method:** `POST`
- **Path:** `/campaigns/{{CampaignID}}/schedule.json`
- **Base URL:** `https://api.moosend.com/v3`
- **Official documentation:** [Schedule Campaign](https://docs.moosend.com/api-documentation/articles/KnowledgeBase/54609-Schedule-a-campaign?lang=en_US)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `CampaignID` | path | `string` | yes | The ID of the campaign that you want to schedule. |
| `DateTime` | body | `date` | yes | The specific date and time the campaign is scheduled to be delivered. Use the same format that you have in the Time and date settings in your account. For example, dd-mm-yyyy . |
| `Timezone` | body | `string` | no | The time zone of your specified date and time. If you don't specify any timezone value , the time zone in your time and date settings  is used. |
