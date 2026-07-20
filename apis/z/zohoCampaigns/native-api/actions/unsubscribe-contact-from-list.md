# Unsubscribe Contact from List with Zoho Campaigns

Unsubscribes a contact from a Zoho Campaigns list.

## Endpoint

- **Method:** `POST`
- **Path:** `/json/listunsubscribe`
- **Base URL:** `https://campaigns.zoho.com/api/v1.1`
- **Official documentation:** [Unsubscribe Contact from List](https://www.zoho.com/campaigns/help/developers/contact-unsubscribe.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `listkey` | query | `list<string>` | yes | List key to unsubscribe the contact from. |
| `contactinfo` | query | `string` | yes | Contact payload in Zoho's documented JSON-style string format. |
| `topic_id` | query | `list<string>` | no | Topic ID required on accounts that use Zoho's updated topic management. |
