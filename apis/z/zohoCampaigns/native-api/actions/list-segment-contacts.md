# List Segment Contacts with Zoho Campaigns

Retrieves contacts from a Zoho Campaigns segment.

## Endpoint

- **Method:** `GET`
- **Path:** `/getsegmentcontacts`
- **Base URL:** `https://campaigns.zoho.com/api/v1.1`
- **Official documentation:** [List Segment Contacts](https://www.zoho.com/campaigns/help/developers/get-segment-contacts.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cvid` | query | `string` | yes | Segment ID (`cvid`) to read contacts from. |
