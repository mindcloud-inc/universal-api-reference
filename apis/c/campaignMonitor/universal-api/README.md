# <img src="https://images.mindcloud.co/apps/icons/campaign-monitor_1773163893926.png" alt="Campaign Monitor logo" width="28" height="28"> Campaign Monitor: Universal API

Email marketing platform for managing clients, lists, subscribers, campaigns, segments, templates, and reporting through the Campaign Monitor API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/campaignMonitor/latest
- **Category:** Marketing
- **Actions:** 32
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.campaignmonitor.com/
- **Vendor API docs:** https://www.campaignmonitor.com/api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Clients](actions/list-clients.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/campaignMonitor/latest/actions/list-clients?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (32)

### Campaign

| Action | Method | Description |
| --- | --- | --- |
| [Create Draft Campaign](actions/create-draft-campaign.md) | POST | Creates a draft campaign in Campaign Monitor. |
| [Delete Campaign](actions/delete-campaign.md) | DELETE | Deletes an existing campaign from Campaign Monitor. |
| [Get Campaign Summary](actions/get-campaign-summary.md) | GET | Retrieves summary metrics for a sent Campaign Monitor campaign. |
| [Send Draft Campaign](actions/send-draft-campaign.md) | PUT | Sends a draft campaign in Campaign Monitor. |

### Campaigns

| Action | Method | Description |
| --- | --- | --- |
| [List Draft Campaigns](actions/list-draft-campaigns.md) | GET | Retrieves draft campaigns for a Campaign Monitor client. |
| [List Scheduled Campaigns](actions/list-scheduled-campaigns.md) | GET | Retrieves scheduled campaigns for a Campaign Monitor client. |
| [List Sent Campaigns](actions/list-sent-campaigns.md) | GET | Retrieves sent campaigns for a Campaign Monitor client. |

### Client

| Action | Method | Description |
| --- | --- | --- |
| [List Clients](actions/list-clients.md) | GET | Retrieves clients in the authenticated Campaign Monitor account. |

### Companies

| Action | Method | Description |
| --- | --- | --- |
| [Get Client Details](actions/get-client-details.md) | GET | Retrieves details for a Campaign Monitor client. |

### List

| Action | Method | Description |
| --- | --- | --- |
| [Create List](actions/create-list.md) | POST | Creates a new list in Campaign Monitor. |
| [Delete List](actions/delete-list.md) | DELETE | Deletes an existing list from Campaign Monitor. |
| [Get List Details](actions/get-list-details.md) | GET | Retrieves details for a Campaign Monitor list. |
| [Get List Stats](actions/get-list-stats.md) | GET | Retrieves statistics for a Campaign Monitor list. |
| [List Custom Fields](actions/list-custom-fields.md) | GET | Retrieves custom fields for a Campaign Monitor list. |
| [Update List](actions/update-list.md) | PUT | Updates an existing list in Campaign Monitor. |

### Lists

| Action | Method | Description |
| --- | --- | --- |
| [List Subscriber Lists](actions/list-subscriber-lists.md) | GET | Retrieves subscriber lists for a Campaign Monitor client. |

### Segment

| Action | Method | Description |
| --- | --- | --- |
| [Create Segment](actions/create-segment.md) | POST | Creates a new segment in Campaign Monitor. |
| [Delete Segment](actions/delete-segment.md) | DELETE | Deletes an existing segment from Campaign Monitor. |
| [Get Segment Details](actions/get-segment-details.md) | GET | Retrieves details for a Campaign Monitor segment. |
| [Update Segment](actions/update-segment.md) | PUT | Updates an existing segment in Campaign Monitor. |

### Segments

| Action | Method | Description |
| --- | --- | --- |
| [List Segments](actions/list-segments.md) | GET | Retrieves segments for a Campaign Monitor client. |

### Subscriber

| Action | Method | Description |
| --- | --- | --- |
| [Add Subscriber](actions/add-subscriber.md) | POST | Adds a subscriber to a Campaign Monitor list, or updates an existing one. |
| [Delete Subscriber](actions/delete-subscriber.md) | DELETE | Deletes a subscriber from a Campaign Monitor list by email address. |
| [Get Subscriber Details](actions/get-subscriber-details.md) | GET | Retrieves a Campaign Monitor subscriber by email address. |
| [List Active Subscribers](actions/list-active-subscribers.md) | GET | Retrieves active subscribers from a Campaign Monitor list. |
| [List Bounced Subscribers](actions/list-bounced-subscribers.md) | GET | Retrieves bounced subscribers from a Campaign Monitor list. |
| [List Deleted Subscribers](actions/list-deleted-subscribers.md) | GET | Retrieves deleted subscribers from a Campaign Monitor list. |
| [List Subscriber History](actions/list-subscriber-history.md) | GET | Retrieves history for a Campaign Monitor subscriber by email address. |
| [List Unconfirmed Subscribers](actions/list-unconfirmed-subscribers.md) | GET | Retrieves unconfirmed subscribers from a Campaign Monitor list. |
| [List Unsubscribed Subscribers](actions/list-unsubscribed-subscribers.md) | GET | Retrieves unsubscribed subscribers from a Campaign Monitor list. |
| [Update Subscriber](actions/update-subscriber.md) | PUT | Updates an existing subscriber in a Campaign Monitor list. |

### Templates

| Action | Method | Description |
| --- | --- | --- |
| [List Templates](actions/list-templates.md) | GET | Retrieves templates for a Campaign Monitor client. |

