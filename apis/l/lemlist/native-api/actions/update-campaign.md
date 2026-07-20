# Update Campaign with lemlist

Updates an existing campaign in lemlist.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/campaigns/:campaignId`
- **Base URL:** `https://api.lemlist.com/api`
- **Official documentation:** [Update Campaign](https://developer.lemlist.com/api-reference/endpoints/campaigns/update-campaign)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaignId` | path | `string` | yes | The ID of the campaign to update. |
| `name` | body | `string` | no | The updated campaign name. |
| `stopOnEmailReplied` | body | `boolean` | no | Pause or stop the campaign when a lead replies by email. |
| `stopOnMeetingBooked` | body | `boolean` | no | Pause or stop the campaign when a meeting is booked. |
| `stopOnLinkClicked` | body | `boolean` | no | Pause or stop the campaign when a lead clicks a link. |
| `stopOnLinkClickedFilter` | body | `string` | no | Restrict the link-click stop rule using the documented filter value. |
| `leadsPausedByInterest` | body | `boolean` | no | Pause leads automatically when they are marked as interested. |
| `opportunityReplied` | body | `boolean` | no | Update the campaign opportunity stage when a reply is received. |
| `opportunityClicked` | body | `boolean` | no | Update the campaign opportunity stage when a tracked link is clicked. |
| `autoLeadInterest` | body | `boolean` | no | Automatically score or infer lead interest from campaign activity. |
| `disableTrackOpen` | body | `boolean` | no | Disable open tracking for this campaign. |
| `disableTrackClick` | body | `boolean` | no | Disable click tracking for this campaign. |
| `disableTrackReply` | body | `boolean` | no | Disable reply tracking for this campaign. |
