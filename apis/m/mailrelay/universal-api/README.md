# <img src="https://images.mindcloud.co/apps/icons/mailrelay_1775665894143.png" alt="Mailrelay logo" width="28" height="28"> Mailrelay: Universal API

Mailrelay is an email marketing and transactional email platform for managing subscribers, campaigns, senders, and delivery reporting through a REST API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/mailrelay/latest
- **Category:** Communication / Email Communications
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://mailrelay.com/
- **Vendor API docs:** https://apidocs.mailrelay.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Ping](actions/ping.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mailrelay/latest/actions/ping?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Campaign

| Action | Method | Description |
| --- | --- | --- |
| [Create Campaign](actions/create-campaign.md) | POST | Creates a new campaign in Mailrelay. |
| [Get Campaign](actions/get-campaign.md) | GET | Retrieves campaign details from your Mailrelay account. |
| [List Campaigns](actions/list-campaigns.md) | GET | Retrieves campaigns from your Mailrelay account. |
| [Send Campaign Test](actions/send-campaign-test.md) | POST | Sends a Mailrelay campaign to test email addresses. |
| [Update Campaign](actions/update-campaign.md) | PUT | Updates an existing campaign in Mailrelay. |

### Group

| Action | Method | Description |
| --- | --- | --- |
| [Create Group](actions/create-group.md) | POST | Creates a new subscriber group in Mailrelay. |
| [Get Group](actions/get-group.md) | GET | Retrieves subscriber group details from Mailrelay. |
| [List Groups](actions/list-groups.md) | GET | Retrieves subscriber groups from your Mailrelay account. |
| [Update Group](actions/update-group.md) | PUT | Updates an existing subscriber group in Mailrelay. |

### Package

| Action | Method | Description |
| --- | --- | --- |
| [Get Package Info](actions/get-package-info.md) | GET | Retrieves package details from your Mailrelay account. |

### Ping

| Action | Method | Description |
| --- | --- | --- |
| [Ping](actions/ping.md) | GET | Retrieves API connectivity status from Mailrelay. |

### Sender

| Action | Method | Description |
| --- | --- | --- |
| [Create Sender](actions/create-sender.md) | POST | Creates a new sender in Mailrelay. |
| [List Senders](actions/list-senders.md) | GET | Retrieves sender profiles from your Mailrelay account. |

### Sent Campaign

| Action | Method | Description |
| --- | --- | --- |
| [Get Sent Campaign](actions/get-sent-campaign.md) | GET | Retrieves a sent campaign from Mailrelay. |
| [List Sent Campaigns](actions/list-sent-campaigns.md) | GET | Retrieves sent campaigns from your Mailrelay account. |
| [Send Campaign](actions/send-campaign.md) | POST | Sends a Mailrelay campaign to its selected audience. |

### Sent Email

| Action | Method | Description |
| --- | --- | --- |
| [Send Email](actions/send-email.md) | POST | Sends an email to one or more recipients through Mailrelay. |

### Stats

| Action | Method | Description |
| --- | --- | --- |
| [Get Stats Summary](actions/get-stats-summary.md) | GET | Retrieves account stats summary from Mailrelay. |

### Subscriber

| Action | Method | Description |
| --- | --- | --- |
| [Bulk Update Subscribers](actions/bulk-update-subscribers.md) | PUT | Updates multiple subscriber records in Mailrelay. |
| [Create Subscriber](actions/create-subscriber.md) | POST | Creates a new subscriber in Mailrelay. |
| [Get Subscriber](actions/get-subscriber.md) | GET | Retrieves subscriber details from your Mailrelay account. |
| [List Subscribers](actions/list-subscribers.md) | GET | Retrieves subscribers from your Mailrelay account. |
| [Sync Subscriber](actions/sync-subscriber.md) | POST | Finds a subscriber in Mailrelay, or creates one if no match is found. |
| [Update Subscriber](actions/update-subscriber.md) | PUT | Updates an existing subscriber in Mailrelay. |

