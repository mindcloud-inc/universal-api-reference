# <img src="https://images.mindcloud.co/apps/icons/sequenzy_1775137598622.png" alt="Sequenzy logo" width="28" height="28"> Sequenzy: Universal API

Sequenzy is an email automation and transactional messaging platform. This app manages subscribers, tags, events, sequences, transactional templates, analytics, and preferences-token generation through the official Sequenzy API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/sequenzy/latest
- **Category:** Marketing
- **Actions:** 28
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.sequenzy.com
- **Vendor API docs:** https://docs.sequenzy.com/api-reference/introduction

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Account Metrics](actions/get-account-metrics.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sequenzy/latest/actions/get-account-metrics?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (28)

### Access Tokens

| Action | Method | Description |
| --- | --- | --- |
| [Get Preferences Token](actions/get-preferences-token.md) | POST | Creates a preferences token in Sequenzy. |

### Email Templates

| Action | Method | Description |
| --- | --- | --- |
| [List Transactional Emails](actions/list-transactional-emails.md) | GET | Retrieves a list of transactional emails from Sequenzy. |

### Events

| Action | Method | Description |
| --- | --- | --- |
| [Trigger Event](actions/trigger-event.md) | POST | Triggers an event for a subscriber in Sequenzy. |
| [Trigger Events (Bulk)](actions/trigger-events-bulk.md) | POST | Triggers events for multiple subscribers in Sequenzy. |

### Metrics

| Action | Method | Description |
| --- | --- | --- |
| [Get Account Metrics](actions/get-account-metrics.md) | GET | Retrieves account engagement metrics from Sequenzy. |
| [Get Account Metrics (Custom Range)](actions/get-account-metrics-custom-range.md) | GET | Retrieves account engagement metrics from Sequenzy for a custom range. |
| [Get Account Metrics (24h)](actions/get-account-metrics24h.md) | GET | Retrieves 24-hour account engagement metrics from Sequenzy. |
| [Get Account Metrics (30d)](actions/get-account-metrics30d.md) | GET | Retrieves 30-day account engagement metrics from Sequenzy. |
| [Get Recipient Metrics](actions/get-recipient-metrics.md) | GET | Retrieves recipient engagement metrics from Sequenzy. |
| [Get Recipient Metrics by Email](actions/get-recipient-metrics-by-email.md) | GET | Retrieves recipient engagement metrics from Sequenzy by email. |
| [Get Recipient Metrics by Sequence](actions/get-recipient-metrics-by-sequence.md) | GET | Retrieves recipient engagement metrics from Sequenzy for a sequence. |
| [Get Recipient Metrics (30d)](actions/get-recipient-metrics30d.md) | GET | Retrieves 30-day recipient engagement metrics from Sequenzy. |

### Subscribers

| Action | Method | Description |
| --- | --- | --- |
| [Create Subscriber](actions/create-subscriber.md) | POST | Creates a new subscriber in Sequenzy. |
| [Create Subscriber Without Lists](actions/create-subscriber-without-lists.md) | POST | Creates a new subscriber in Sequenzy without assigning lists. |
| [Create Subscriber Without Sequence Enrollment](actions/create-subscriber-without-sequence-enrollment.md) | POST | Creates a new subscriber in Sequenzy without sequence enrollment. |
| [Create Unsubscribed Subscriber](actions/create-unsubscribed-subscriber.md) | POST | Creates an unsubscribed subscriber in Sequenzy. |
| [Delete Subscriber](actions/delete-subscriber.md) | DELETE | Deletes an existing subscriber from Sequenzy. |
| [Get Subscriber](actions/get-subscriber.md) | GET | Retrieves a subscriber from Sequenzy by email address. |
| [List Subscribers](actions/list-subscribers.md) | GET | Retrieves a paginated list of subscribers from Sequenzy. |
| [Merge Subscriber](actions/merge-subscriber.md) | POST | Creates or merges a subscriber in Sequenzy by email. |
| [Overwrite Subscriber](actions/overwrite-subscriber.md) | POST | Creates or overwrites a subscriber in Sequenzy by email. |
| [Unsubscribe Subscriber](actions/unsubscribe-subscriber.md) | PUT | Unsubscribes an existing subscriber in Sequenzy. |
| [Update Subscriber](actions/update-subscriber.md) | PUT | Updates an existing subscriber in Sequenzy. |

### Tags

| Action | Method | Description |
| --- | --- | --- |
| [Add Tag](actions/add-tag.md) | POST | Adds a tag to a subscriber in Sequenzy. |
| [Add Tags (Bulk)](actions/add-tags-bulk.md) | POST | Adds tags to multiple subscribers in Sequenzy. |

### Workflows

| Action | Method | Description |
| --- | --- | --- |
| [Create Sequence with AI](actions/create-sequence-with-ai.md) | POST | Creates an AI-generated sequence in Sequenzy. |
| [Create Sequence with Steps](actions/create-sequence-with-steps.md) | POST | Creates a sequence with explicit steps in Sequenzy. |
| [Get Sequence](actions/get-sequence.md) | GET | Retrieves sequence metadata and steps from Sequenzy. |

