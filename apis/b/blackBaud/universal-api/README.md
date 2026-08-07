# <img src="https://images.mindcloud.co/apps/icons/blackbaud-logo_1786039281632.png" alt="BlackBaud logo" width="28" height="28"> BlackBaud: Universal API

Blackbaud Altru SKY API integration for read-only sales, transactions, and customer data.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/blackBaud/latest
- **Actions:** 22
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.blackbaud.com/
- **Vendor API docs:** https://developer.blackbaud.com/skyapi/docs/getting-started

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Action](actions/get-action.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/blackBaud/latest/actions/get-action?connectionId=$CONNECTION_ID&actionId=Action%20ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (22)

### Activities

| Action | Method | Description |
| --- | --- | --- |
| [Get Action](actions/get-action.md) | GET |  |
| [Get Actions](actions/get-actions.md) | GET |  |
| [Get Constituent Actions](actions/get-constituent-actions.md) | GET |  |

### Campaigns

| Action | Method | Description |
| --- | --- | --- |
| [Get Campaign](actions/get-campaign.md) | GET |  |
| [Get Campaigns](actions/get-campaigns.md) | GET |  |

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [Get Constituent](actions/get-constituent.md) | GET |  |
| [Get Constituents](actions/get-constituents.md) | GET |  |
| [Search Constituents](actions/search-constituents.md) | GET |  |
| [Search Constituents Duplicate](actions/search-constituents-duplicate.md) | GET |  |
| [Search For A Constituent](actions/search-for-a-constituent.md) | GET |  |

### Currency

| Action | Method | Description |
| --- | --- | --- |
| [List Currencies](actions/list-currencies.md) | GET |  |

### Event Category

| Action | Method | Description |
| --- | --- | --- |
| [Get Event Categories](actions/get-event-categories.md) | GET |  |

### Events

| Action | Method | Description |
| --- | --- | --- |
| [Get Events](actions/get-events.md) | GET |  |

### Fund

| Action | Method | Description |
| --- | --- | --- |
| [Get Fund](actions/get-fund.md) | GET |  |
| [Get Funds](actions/get-funds.md) | GET |  |

### Gift

| Action | Method | Description |
| --- | --- | --- |
| [Get Gift](actions/get-gift.md) | GET |  |
| [Get Gifts](actions/get-gifts.md) | GET |  |

### Order Patron View

| Action | Method | Description |
| --- | --- | --- |
| [View Order Patron](actions/view-order-patron.md) | GET |  |

### Order Ticket Detail

| Action | Method | Description |
| --- | --- | --- |
| [List Order Ticket Details](actions/list-order-ticket-details.md) | GET |  |

### Orders

| Action | Method | Description |
| --- | --- | --- |
| [Get Order Delivery Information](actions/get-order-delivery-information.md) | GET |  |

### Phone Type

| Action | Method | Description |
| --- | --- | --- |
| [Get Phone Types](actions/get-phone-types.md) | GET |  |

### Tickets

| Action | Method | Description |
| --- | --- | --- |
| [List Sales Order Tickets Without Refunds](actions/list-sales-order-tickets-without-refunds.md) | GET |  |

