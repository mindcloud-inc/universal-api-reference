# <img src="https://images.mindcloud.co/apps/icons/webinar-geek_1773334492125.png" alt="WebinarGeek logo" width="28" height="28"> WebinarGeek: Universal API

Manage webinars, broadcasts, subscribers, and webinar engagement

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/webinarGeek/latest
- **Category:** Communication / Video Communications
- **Actions:** 11
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.webinargeek.com
- **Vendor API docs:** https://webinargeek.docs.apiary.io/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Retrieve Account Metadata](actions/retrieve-account-metadata.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/webinarGeek/latest/actions/retrieve-account-metadata?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (11)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve Account Metadata](actions/retrieve-account-metadata.md) | GET |  |

### Broadcast

| Action | Method | Description |
| --- | --- | --- |
| [List Broadcasts](actions/list-broadcasts.md) | GET |  |
| [Retrieve Broadcast](actions/retrieve-broadcast.md) | GET |  |

### Message

| Action | Method | Description |
| --- | --- | --- |
| [List Messages](actions/list-messages.md) | GET |  |

### Payment

| Action | Method | Description |
| --- | --- | --- |
| [List Subscription Payments](actions/list-subscription-payments.md) | GET |  |

### Question

| Action | Method | Description |
| --- | --- | --- |
| [List Questions](actions/list-questions.md) | GET |  |

### Subscription

| Action | Method | Description |
| --- | --- | --- |
| [List Subscriptions](actions/list-subscriptions.md) | GET |  |
| [Retrieve Subscription](actions/retrieve-subscription.md) | GET |  |
| [Subscribe to Broadcast](actions/subscribe-to-broadcast.md) | POST |  |

### Webinar

| Action | Method | Description |
| --- | --- | --- |
| [List Webinars](actions/list-webinars.md) | GET |  |
| [Retrieve Webinar](actions/retrieve-webinar.md) | GET |  |

