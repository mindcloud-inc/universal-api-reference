# Subscribe Contact to List with Zoho Campaigns

Subscribes a contact to a Zoho Campaigns list.

## Endpoint

- **Method:** `POST`
- **Path:** `/json/listsubscribe`
- **Base URL:** `https://campaigns.zoho.com/api/v1.1`
- **Official documentation:** [Subscribe Contact to List](https://www.zoho.com/campaigns/help/developers/contact-subscribe.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `listkey` | query | `list<string>` | yes | List key to subscribe the contact to. |
| `contactinfo` | query | `string` | yes | Contact payload in Zoho's documented JSON-style string format. |
| `source` | query | `string` | no | Optional source label recorded for the contact. |
| `topic_id` | query | `list<string>` | no | Topic ID required on accounts that use Zoho's updated topic management. |
