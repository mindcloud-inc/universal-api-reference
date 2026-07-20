# <img src="https://images.mindcloud.co/apps/icons/sendloop_1775585635583.png" alt="Sendloop logo" width="28" height="28"> Sendloop: Universal API

Manage subscribers, lists, campaigns, and email reports

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/sendloop/latest
- **Category:** Communication / Email Communications
- **Actions:** 20
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://sendloop.com/
- **Vendor API docs:** https://chmyos.notion.site/API-reference-eaa4fa70940b4daa928bde3dbf2245a5

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Lists](actions/list-lists.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sendloop/latest/actions/list-lists?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (20)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Get Account Info](actions/get-account-info.md) | GET |  |
| [Update Account Info](actions/update-account-info.md) | PUT |  |

### Campaign

| Action | Method | Description |
| --- | --- | --- |
| [Create Campaign](actions/create-campaign.md) | POST |  |
| [Get Campaign](actions/get-campaign.md) | GET |  |
| [List Campaigns](actions/list-campaigns.md) | GET |  |
| [List Campaigns by Status](actions/list-campaigns-by-status.md) | GET |  |
| [Update Campaign](actions/update-campaign.md) | PUT |  |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Get Subscriber](actions/get-subscriber.md) | GET |  |
| [Import Subscribers](actions/import-subscribers.md) | POST |  |
| [List Subscribers](actions/list-subscribers.md) | GET |  |
| [Search Subscribers](actions/search-subscribers.md) | GET |  |
| [Subscribe Email Address](actions/subscribe-email-address.md) | POST |  |
| [Unsubscribe Subscriber](actions/unsubscribe-subscriber.md) | PUT |  |
| [Update Subscriber](actions/update-subscriber.md) | PUT |  |

### List

| Action | Method | Description |
| --- | --- | --- |
| [Create List](actions/create-list.md) | POST |  |
| [Get List](actions/get-list.md) | GET |  |
| [Get List Settings](actions/get-list-settings.md) | GET |  |
| [List Lists](actions/list-lists.md) | GET |  |
| [Update List](actions/update-list.md) | PUT |  |
| [Update List Settings](actions/update-list-settings.md) | PUT |  |

