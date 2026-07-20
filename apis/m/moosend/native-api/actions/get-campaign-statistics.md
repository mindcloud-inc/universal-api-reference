# Get Campaign Statistics with Moosend

Retrieves campaign statistics from Moosend.

## Endpoint

- **Method:** `GET`
- **Path:** `/campaigns/{{CampaignID}}/stats/{{Type}}.json`
- **Base URL:** `https://api.moosend.com/v3`
- **Official documentation:** [Get Campaign Statistics](https://docs.moosend.com/api-documentation/articles/KnowledgeBase/54605-Get-campaign-statistics?lang=en_US)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `CampaignID` | path | `string` | yes | The ID of the campaign that you are fetching statistics for. |
| `Type` | path | `string` | no | The type of activity used to get information and display statistics. Possible values are: Sent - when and to which recipients the campaign was sent. Opened - who opened the campaign. LinkClicked - who clicked on which links in the campaign. Unsubscribed - who unsubscribed from the campaign by clicking the unsubscribe link and when. Bounced - which email recipients failed to receive the campaign. If not specified, Sent value is used by default. Complained - which email recipients reported your campaign as spam through their email service. Activity - all types of activities for the campaign. |
| `date` | query | `date` | no | The specific year, month, and day the activity occurred. The date has a YYYY/MM/DD format. |
