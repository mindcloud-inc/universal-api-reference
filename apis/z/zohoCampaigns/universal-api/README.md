# <img src="https://images.mindcloud.co/apps/icons/images-1_1773349494626.png" alt="Zoho Campaigns logo" width="28" height="28"> Zoho Campaigns: Universal API

Create, send, and track email marketing campaigns

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/zohoCampaigns/latest
- **Category:** Marketing
- **Actions:** 23
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.zoho.com/campaigns/
- **Vendor API docs:** https://www.zoho.com/campaigns/help/developers/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Mailing Lists](actions/list-mailing-lists.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoCampaigns/latest/actions/list-mailing-lists?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (23)

### Campaign

| Action | Method | Description |
| --- | --- | --- |
| [Create Campaign](actions/create-campaign.md) | POST | Creates a campaign in Zoho Campaigns. |
| [Get Campaign Details](actions/get-campaign-details.md) | GET | Retrieves campaign details from Zoho Campaigns. |
| [Get Last Campaign Report](actions/get-last-campaign-report.md) | GET | Retrieves the last campaign report from Zoho Campaigns. |
| [List Campaign Reports](actions/list-campaign-reports.md) | GET | Retrieves campaign reports from Zoho Campaigns. |
| [List Recent Campaigns](actions/list-recent-campaigns.md) | GET | Retrieves recent campaigns from Zoho Campaigns. |
| [List Recently Sent Campaigns](actions/list-recently-sent-campaigns.md) | GET | Retrieves recently sent campaigns from Zoho Campaigns. |
| [Schedule Campaign](actions/schedule-campaign.md) | PUT | Schedules a campaign in Zoho Campaigns. |
| [Send Campaign](actions/send-campaign.md) | PUT | Sends a campaign in Zoho Campaigns. |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Add List Contacts in Bulk](actions/add-list-contacts-in-bulk.md) | POST | Adds contacts to a Zoho Campaigns list in bulk. |
| [Get Campaign Recipients Data](actions/get-campaign-recipients-data.md) | GET | Retrieves campaign recipient data from Zoho Campaigns. |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves contacts from a Zoho Campaigns list. |
| [Subscribe Contact to List](actions/subscribe-contact-to-list.md) | POST | Subscribes a contact to a Zoho Campaigns list. |
| [Unsubscribe Contact from List](actions/unsubscribe-contact-from-list.md) | PUT | Unsubscribes a contact from a Zoho Campaigns list. |

### Contact Field

| Action | Method | Description |
| --- | --- | --- |
| [List Contact Fields](actions/list-contact-fields.md) | GET | Retrieves all contact fields from Zoho Campaigns. |

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [List Segment Contacts](actions/list-segment-contacts.md) | GET | Retrieves contacts from a Zoho Campaigns segment. |
| [Move Contact to Do Not Mail](actions/move-contact-to-do-not-mail.md) | PUT | Moves a contact to Zoho Campaigns do-not-mail. |

### List

| Action | Method | Description |
| --- | --- | --- |
| [Add New List and Contacts](actions/add-new-list-and-contacts.md) | POST | Creates a mailing list and contacts in Zoho Campaigns. |
| [Get Total Contacts](actions/get-total-contacts.md) | GET | Retrieves total contacts from a Zoho Campaigns list. |

### Lists

| Action | Method | Description |
| --- | --- | --- |
| [Update List Details](actions/update-list-details.md) | PUT | Updates a Zoho Campaigns mailing list. |

### Mailing List

| Action | Method | Description |
| --- | --- | --- |
| [List Mailing Lists](actions/list-mailing-lists.md) | GET | Retrieves mailing lists from Zoho Campaigns. |

### Segments

| Action | Method | Description |
| --- | --- | --- |
| [Get Segment Details](actions/get-segment-details.md) | GET | Retrieves segment details from Zoho Campaigns. |

### Tags

| Action | Method | Description |
| --- | --- | --- |
| [Create Topics](actions/create-topics.md) | POST | Creates marketing topics in Zoho Campaigns. |
| [List Topics](actions/list-topics.md) | GET | Retrieves marketing topics from Zoho Campaigns. |

