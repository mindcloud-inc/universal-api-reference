# <img src="https://images.mindcloud.co/apps/icons/sender_1773248911731.png" alt="Sender logo" width="28" height="28"> Sender: Universal API

Sender: Create campaigns, automate email and SMS, and manage subscribers

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/sender/latest
- **Category:** Marketing
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.sender.net/
- **Vendor API docs:** https://api.sender.net/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Fields](actions/list-fields.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sender/latest/actions/list-fields?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Campaigns

| Action | Method | Description |
| --- | --- | --- |
| [Create Campaign](actions/create-campaign.md) | POST |  |
| [Create Transactional Campaign](actions/create-transactional-campaign.md) | POST |  |
| [Get Campaign](actions/get-campaign.md) | GET |  |
| [Get Transactional Campaign](actions/get-transactional-campaign.md) | GET |  |
| [List Campaigns](actions/list-campaigns.md) | GET |  |
| [Schedule Send](actions/schedule-send.md) | PUT |  |
| [Send Campaign](actions/send-campaign.md) | PUT |  |

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [Create Subscriber](actions/create-subscriber.md) | POST |  |
| [Delete Subscriber](actions/delete-subscriber.md) | DELETE |  |
| [Get Subscriber](actions/get-subscriber.md) | GET |  |
| [List Subscribers](actions/list-subscribers.md) | GET |  |
| [List Subscribers in Group](actions/list-subscribers-in-group.md) | GET |  |
| [Update Subscriber](actions/update-subscriber.md) | PUT |  |

### Emails

| Action | Method | Description |
| --- | --- | --- |
| [Send Transactional Email Without Template](actions/send-transactional-email-without-template.md) | POST |  |

### Events

| Action | Method | Description |
| --- | --- | --- |
| [List Subscriber Events](actions/list-subscriber-events.md) | GET |  |

### Field

| Action | Method | Description |
| --- | --- | --- |
| [List Fields](actions/list-fields.md) | GET |  |

### Lists

| Action | Method | Description |
| --- | --- | --- |
| [Add Subscriber to Group](actions/add-subscriber-to-group.md) | PUT |  |
| [Create Group](actions/create-group.md) | POST |  |
| [Get Group](actions/get-group.md) | GET |  |
| [List Groups](actions/list-groups.md) | GET |  |
| [List Segments](actions/list-segments.md) | GET |  |
| [Remove Subscriber from Group](actions/remove-subscriber-from-group.md) | PUT |  |
| [Rename Group](actions/rename-group.md) | PUT |  |

### Transactional Campaign

| Action | Method | Description |
| --- | --- | --- |
| [List Transactional Campaigns](actions/list-transactional-campaigns.md) | GET |  |

