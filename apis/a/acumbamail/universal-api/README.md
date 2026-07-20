# <img src="https://images.mindcloud.co/apps/icons/acumbamail_1775238070331.png" alt="Acumbamail logo" width="28" height="28"> Acumbamail: Universal API

Acumbamail: Manage email campaigns, subscribers, SMS, and webhooks

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/acumbamail/latest
- **Category:** Marketing
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://acumbamail.com
- **Vendor API docs:** https://acumbamail.com/apidoc/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Lists](actions/list-lists.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/acumbamail/latest/actions/list-lists?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Campaigns

| Action | Method | Description |
| --- | --- | --- |
| [Create Campaign](actions/create-campaign.md) | POST | Creates and sends a campaign in Acumbamail. |
| [Get Campaign Basic Information](actions/get-campaign-basic-information.md) | GET | Retrieves basic campaign information from Acumbamail. |
| [Get Campaign Total Information](actions/get-campaign-total-information.md) | GET | Retrieves complete campaign information from Acumbamail. |
| [List Campaign Clicks](actions/list-campaign-clicks.md) | GET | Retrieves campaign click activity from Acumbamail. |
| [List Campaign Links](actions/list-campaign-links.md) | GET | Retrieves campaign links and clicks from Acumbamail. |
| [List Campaigns](actions/list-campaigns.md) | GET | Retrieves created campaign names and IDs from Acumbamail. |
| [Send Template Campaign](actions/send-template-campaign.md) | POST | Creates and sends a template campaign in Acumbamail. |

### Forms

| Action | Method | Description |
| --- | --- | --- |
| [List Forms](actions/list-forms.md) | GET | Retrieves forms for a subscriber list in Acumbamail. |

### List

| Action | Method | Description |
| --- | --- | --- |
| [Configure List Webhook](actions/configure-list-webhook.md) | PUT | Updates list webhook settings in Acumbamail. |
| [Get List Webhook](actions/get-list-webhook.md) | GET | Retrieves list webhook settings from Acumbamail. |

### Lists

| Action | Method | Description |
| --- | --- | --- |
| [Create List](actions/create-list.md) | POST | Creates a subscriber list in Acumbamail. |
| [Get List Stats](actions/get-list-stats.md) | GET | Retrieves subscriber list statistics from Acumbamail. |
| [List List Segments](actions/list-list-segments.md) | GET | Retrieves subscriber list segments from Acumbamail. |
| [List Lists](actions/list-lists.md) | GET | Retrieves available subscriber lists from Acumbamail. |

### Sms

| Action | Method | Description |
| --- | --- | --- |
| [List SMS Campaigns](actions/list-sms-campaigns.md) | GET | Retrieves SMS campaign summaries from Acumbamail. |
| [Send SMS](actions/send-sms.md) | POST | Sends one or more SMS messages from Acumbamail. |

### Subscribers

| Action | Method | Description |
| --- | --- | --- |
| [Add Subscriber](actions/add-subscriber.md) | POST | Creates a subscriber in an Acumbamail list. |
| [Batch Add Subscribers](actions/batch-add-subscribers.md) | POST | Creates subscribers in an Acumbamail list in bulk. |
| [Delete Subscriber](actions/delete-subscriber.md) | DELETE | Deletes a subscriber from an Acumbamail list. |
| [Get Subscriber Details](actions/get-subscriber-details.md) | GET | Retrieves detailed subscriber information from Acumbamail. |
| [List Subscribers](actions/list-subscribers.md) | GET | Retrieves subscribers from an Acumbamail list. |
| [Search Subscriber](actions/search-subscriber.md) | GET | Finds a subscriber across Acumbamail lists by email. |
| [Unsubscribe Subscriber](actions/unsubscribe-subscriber.md) | PUT | Updates a subscriber to unsubscribe from an Acumbamail list. |

### Templates

| Action | Method | Description |
| --- | --- | --- |
| [List Templates](actions/list-templates.md) | GET | Retrieves campaign templates and availability from Acumbamail. |

