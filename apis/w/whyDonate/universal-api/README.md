# <img src="https://images.mindcloud.co/apps/icons/why-donate_1774377378101.png" alt="WhyDonate logo" width="28" height="28"> WhyDonate: Universal API

Create fundraisers, collect donations, and manage donation widgets

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/whyDonate/latest
- **Category:** Commerce / Payments & Billing
- **Actions:** 8
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://whydonate.com
- **Vendor API docs:** https://helpdesk.whydonate.com/en/category/donation-button-plugin-jwsieg/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Widget Styles](actions/list-widget-styles.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/whyDonate/latest/actions/list-widget-styles?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (8)

### Campaigns

| Action | Method | Description |
| --- | --- | --- |
| [Get Donation Values](actions/get-donation-values.md) | GET |  |
| [Get Fundraiser Details](actions/get-fundraiser-details.md) | GET |  |
| [Get Widget Donation Values](actions/get-widget-donation-values.md) | GET |  |
| [List User Fundraisers](actions/list-user-fundraisers.md) | GET |  |

### Checkouts

| Action | Method | Description |
| --- | --- | --- |
| [Get Payment Status](actions/get-payment-status.md) | GET |  |

### Collections

| Action | Method | Description |
| --- | --- | --- |
| [List Widget Shortcodes](actions/list-widget-shortcodes.md) | GET |  |
| [List Widget Styles](actions/list-widget-styles.md) | GET |  |

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [Get Widget Style](actions/get-widget-style.md) | GET |  |

