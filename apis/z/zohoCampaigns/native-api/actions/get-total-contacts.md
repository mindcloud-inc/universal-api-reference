# Get Total Contacts with Zoho Campaigns

Retrieves total contacts from a Zoho Campaigns list.

## Endpoint

- **Method:** `GET`
- **Path:** `/listsubscriberscount`
- **Base URL:** `https://campaigns.zoho.com/api/v1.1`
- **Official documentation:** [Get Total Contacts](https://www.zoho.com/campaigns/help/developers/view-total-contacts.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `listkey` | query | `string` | yes | Mailing list key to count subscribers for. |
| `status` | query | `string` | no | Subscriber status to count. Accepted values: `0`, `1`, `2`, `3`. |
