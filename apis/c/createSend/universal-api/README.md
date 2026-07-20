# <img src="https://images.mindcloud.co/apps/icons/44748_1774628733846.png" alt="CreateSend logo" width="28" height="28"> CreateSend: Universal API

Email marketing platform for managing clients, subscriber lists, segments, campaigns, templates, and reports through the Campaign Monitor CreateSend API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/createSend/latest
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
curl -X GET "https://connect.mindcloud.co/v1/universal/createSend/latest/actions/list-clients?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (32)

### Campaign

| Action | Method | Description |
| --- | --- | --- |
| [Create Draft Campaign](actions/create-draft-campaign.md) | POST | Creates a draft campaign in CreateSend. |
| [Delete Campaign](actions/delete-campaign.md) | DELETE | Deletes an existing campaign from CreateSend. |
| [Get Campaign Summary](actions/get-campaign-summary.md) | GET | Retrieves a campaign summary from CreateSend. |
| [Send Draft Campaign](actions/send-draft-campaign.md) | PUT | Sends a draft campaign in CreateSend. |

### Campaigns

| Action | Method | Description |
| --- | --- | --- |
| [List Draft Campaigns](actions/list-draft-campaigns.md) | GET | Retrieves draft campaigns for a client in CreateSend. |
| [List Scheduled Campaigns](actions/list-scheduled-campaigns.md) | GET | Retrieves scheduled campaigns for a client in CreateSend. |
| [List Sent Campaigns](actions/list-sent-campaigns.md) | GET | Retrieves sent campaigns for a client in CreateSend. |

### Client

| Action | Method | Description |
| --- | --- | --- |
| [Get Client Details](actions/get-client-details.md) | GET | Retrieves client details from CreateSend. |
| [List Clients](actions/list-clients.md) | GET | Retrieves clients from CreateSend. |

### List

| Action | Method | Description |
| --- | --- | --- |
| [Create List](actions/create-list.md) | POST | Creates a new list in CreateSend. |
| [Delete List](actions/delete-list.md) | DELETE | Deletes an existing list from CreateSend. |
| [Get List Details](actions/get-list-details.md) | GET | Retrieves list details from CreateSend. |
| [Get List Stats](actions/get-list-stats.md) | GET | Retrieves list stats from CreateSend. |
| [List Custom Fields](actions/list-custom-fields.md) | GET | Retrieves custom fields for a list in CreateSend. |
| [Update List](actions/update-list.md) | PUT | Updates an existing list in CreateSend. |

### Lists

| Action | Method | Description |
| --- | --- | --- |
| [List Subscriber Lists](actions/list-subscriber-lists.md) | GET | Retrieves subscriber lists for a client in CreateSend. |

### Segment

| Action | Method | Description |
| --- | --- | --- |
| [Create Segment](actions/create-segment.md) | POST | Creates a new segment in CreateSend. |
| [Delete Segment](actions/delete-segment.md) | DELETE | Deletes an existing segment from CreateSend. |
| [Get Segment Details](actions/get-segment-details.md) | GET | Retrieves segment details from CreateSend. |
| [Update Segment](actions/update-segment.md) | PUT | Updates an existing segment in CreateSend. |

### Segments

| Action | Method | Description |
| --- | --- | --- |
| [List Segments](actions/list-segments.md) | GET | Retrieves segments for a client in CreateSend. |

### Subscriber

| Action | Method | Description |
| --- | --- | --- |
| [Add Subscriber](actions/add-subscriber.md) | POST | Creates a new subscriber in CreateSend. |
| [Delete Subscriber](actions/delete-subscriber.md) | DELETE | Deletes an existing subscriber from CreateSend by email address. |
| [Get Subscriber Details](actions/get-subscriber-details.md) | GET | Retrieves subscriber details from CreateSend by email address. |
| [Get Subscriber History](actions/get-subscriber-history.md) | GET | Retrieves subscriber history from CreateSend by email address. |
| [List Active Subscribers](actions/list-active-subscribers.md) | GET | Retrieves active subscribers for a list in CreateSend. |
| [List Bounced Subscribers](actions/list-bounced-subscribers.md) | GET | Retrieves bounced subscribers for a list in CreateSend. |
| [List Deleted Subscribers](actions/list-deleted-subscribers.md) | GET | Retrieves deleted subscribers for a list in CreateSend. |
| [List Unconfirmed Subscribers](actions/list-unconfirmed-subscribers.md) | GET | Retrieves unconfirmed subscribers for a list in CreateSend. |
| [List Unsubscribed Subscribers](actions/list-unsubscribed-subscribers.md) | GET | Retrieves unsubscribed subscribers for a list in CreateSend. |
| [Update Subscriber](actions/update-subscriber.md) | PUT | Updates an existing subscriber in CreateSend by email address. |

### Templates

| Action | Method | Description |
| --- | --- | --- |
| [List Templates](actions/list-templates.md) | GET | Retrieves templates for a client in CreateSend. |

