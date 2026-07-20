# Add New List and Contacts with Zoho Campaigns

Creates a mailing list and contacts in Zoho Campaigns.

## Endpoint

- **Method:** `POST`
- **Path:** `/addlistandcontacts`
- **Base URL:** `https://campaigns.zoho.com/api/v1.1`
- **Official documentation:** [Add New List and Contacts](https://www.zoho.com/campaigns/help/developers/add-new-list-contact.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `emailids` | query | `string` | yes | Up to ten email addresses to add to the new list. Send multiple values as a string separated by `,`. |
| `listname` | query | `string` | yes | Name of the new mailing list. |
| `signupform` | query | `string` | yes | Signup form visibility for the new list. Accepted values: `0`, `1`. |
| `listdescription` | query | `string` | no | Description for the new mailing list. |
