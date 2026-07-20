# Add List Contacts in Bulk with Zoho Campaigns

Adds contacts to a Zoho Campaigns list in bulk.

## Endpoint

- **Method:** `POST`
- **Path:** `/addlistsubscribersinbulk`
- **Base URL:** `https://campaigns.zoho.com/api/v1.1`
- **Official documentation:** [Add List Contacts in Bulk](https://www.zoho.com/campaigns/help/developers/add-contacts-existing-list.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `listkey` | query | `list<string>` | yes | List key to add contacts to. |
| `emailids` | query | `string` | yes | Up to ten email addresses, separated by commas. Send multiple values as a string separated by `,`. |
