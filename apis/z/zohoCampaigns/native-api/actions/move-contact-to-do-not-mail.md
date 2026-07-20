# Move Contact to Do Not Mail with Zoho Campaigns

Moves a contact to Zoho Campaigns do-not-mail.

## Endpoint

- **Method:** `POST`
- **Path:** `/json/contactdonotmail`
- **Base URL:** `https://campaigns.zoho.com/api/v1.1`
- **Official documentation:** [Move Contact to Do Not Mail](https://www.zoho.com/campaigns/help/developers/do-not-mail.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contactinfo` | query | `string` | yes | Contact payload in Zoho's documented string format. |
