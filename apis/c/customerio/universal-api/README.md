# <img src="https://images.mindcloud.co/apps/icons/favicon_1773066174767.png" alt="Customer.io logo" width="28" height="28"> Customer.io: Universal API

Create journeys, send messages, sync data, and analyze campaign performance.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/customerio/latest
- **Category:** Marketing
- **Actions:** 31
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://customer.io
- **Vendor API docs:** https://docs.customer.io/integrations/api/app/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Workspaces](actions/list-workspaces.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/customerio/latest/actions/list-workspaces?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (31)

### Broadcast

| Action | Method | Description |
| --- | --- | --- |
| [Get Broadcast](actions/get-broadcast.md) | GET | Retrieves a broadcast from Customer.io. |
| [List Broadcasts](actions/list-broadcasts.md) | GET | Retrieves broadcasts from Customer.io. |

### Broadcast Metric

| Action | Method | Description |
| --- | --- | --- |
| [Get Broadcast Metrics](actions/get-broadcast-metrics.md) | GET | Retrieves metrics for a Customer.io broadcast. |

### Campaign

| Action | Method | Description |
| --- | --- | --- |
| [Get Campaign](actions/get-campaign.md) | GET | Retrieves a campaign from Customer.io. |
| [List Campaigns](actions/list-campaigns.md) | GET | Retrieves campaigns from Customer.io. |

### Campaign Metric

| Action | Method | Description |
| --- | --- | --- |
| [Get Campaign Metrics](actions/get-campaign-metrics.md) | GET | Retrieves metrics for a Customer.io campaign. |

### Customer

| Action | Method | Description |
| --- | --- | --- |
| [List Customer Attributes](actions/list-customer-attributes.md) | GET | Retrieves attributes for a customer in Customer.io. |
| [List Customer Messages](actions/list-customer-messages.md) | GET | Retrieves messages sent to a customer in Customer.io. |
| [List Customer Segments](actions/list-customer-segments.md) | GET | Retrieves segments for a customer in Customer.io. |
| [List Customer Subscription Preferences](actions/list-customer-subscription-preferences.md) | GET | Retrieves subscription preferences for a customer in Customer.io. |
| [List Customers, Attributes, and Devices](actions/list-customers-attributes-and-devices.md) | GET | Retrieves customers, attributes, and devices from Customer.io by ID. |
| [List Customers by Email](actions/list-customers-by-email.md) | GET | Finds customers in Customer.io by email address. |
| [Search Customers](actions/search-customers.md) | GET | Finds customers in Customer.io by filter. |

### Customer Activity

| Action | Method | Description |
| --- | --- | --- |
| [List Customer Activities](actions/list-customer-activities.md) | GET | Retrieves activities for a customer in Customer.io. |

### Newsletter

| Action | Method | Description |
| --- | --- | --- |
| [Get Newsletter](actions/get-newsletter.md) | GET | Retrieves a newsletter from Customer.io. |
| [List Newsletters](actions/list-newsletters.md) | GET | Retrieves newsletters from Customer.io. |

### Newsletter Metric

| Action | Method | Description |
| --- | --- | --- |
| [Get Newsletter Metrics](actions/get-newsletter-metrics.md) | GET | Retrieves metrics for a Customer.io newsletter. |

### Segment

| Action | Method | Description |
| --- | --- | --- |
| [Get Segment](actions/get-segment.md) | GET | Retrieves a segment from Customer.io. |
| [Get Segment Customer Count](actions/get-segment-customer-count.md) | GET | Retrieves the customer count for a Customer.io segment. |
| [List Segments](actions/list-segments.md) | GET | Retrieves segments from Customer.io. |

### Segment Member

| Action | Method | Description |
| --- | --- | --- |
| [List Customers in a Segment](actions/list-customers-in-segment.md) | GET | Retrieves customers in a segment from Customer.io. |

### Subscription Topic

| Action | Method | Description |
| --- | --- | --- |
| [List Subscription Topics](actions/list-subscription-topics.md) | GET | Retrieves subscription topics from Customer.io. |

### Transactional Email

| Action | Method | Description |
| --- | --- | --- |
| [Send Transactional Email](actions/send-transactional-email.md) | POST | Sends a transactional email from Customer.io. |

### Transactional Inbox Message

| Action | Method | Description |
| --- | --- | --- |
| [Send Transactional Inbox Message](actions/send-transactional-inbox-message.md) | POST | Sends a transactional inbox message from Customer.io. |

### Transactional Message

| Action | Method | Description |
| --- | --- | --- |
| [Get Transactional Message](actions/get-transactional-message.md) | GET | Retrieves a transactional message from Customer.io. |
| [List Transactional Messages](actions/list-transactional-messages.md) | GET | Retrieves transactional messages from Customer.io. |

### Transactional Message Delivery

| Action | Method | Description |
| --- | --- | --- |
| [Get Transactional Message Deliveries](actions/get-transactional-message-deliveries.md) | GET | Retrieves deliveries for a Customer.io transactional message. |

### Transactional Message Metric

| Action | Method | Description |
| --- | --- | --- |
| [Get Transactional Message Metrics](actions/get-transactional-message-metrics.md) | GET | Retrieves metrics for a Customer.io transactional message. |

### Transactional Push

| Action | Method | Description |
| --- | --- | --- |
| [Send Transactional Push](actions/send-transactional-push.md) | POST | Sends a transactional push message from Customer.io. |

### Transactional Sms

| Action | Method | Description |
| --- | --- | --- |
| [Send Transactional SMS](actions/send-transactional-sms.md) | POST | Sends a transactional SMS from Customer.io. |

### Workspace

| Action | Method | Description |
| --- | --- | --- |
| [List Workspaces](actions/list-workspaces.md) | GET | Retrieves workspaces from Customer.io. |

