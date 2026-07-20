# <img src="https://images.mindcloud.co/apps/icons/hotspot-system_1774373079261.png" alt="HotspotSystem logo" width="28" height="28"> HotspotSystem: Universal API

Cloud-based hotspot management platform for guest Wi-Fi operations, locations, vouchers, subscribers, and access transaction reporting.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/hotspotSystem/latest
- **Category:** IT Operations / IT Service Management
- **Actions:** 14
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.hotspotsystem.com/
- **Vendor API docs:** https://www.hotspotsystem.com/apidocs/api/reference/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Verify Credentials](actions/verify-credentials.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hotspotSystem/latest/actions/verify-credentials?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (14)

### Customer

| Action | Method | Description |
| --- | --- | --- |
| [List Customers](actions/list-customers.md) | GET | Retrieves the resource owner's customers from HotspotSystem. |
| [List Customers by Location](actions/list-customers-by-location.md) | GET | Retrieves customers at a specific location from HotspotSystem. |

### Location

| Action | Method | Description |
| --- | --- | --- |
| [List Locations](actions/list-locations.md) | GET | Retrieves the resource owner's locations from HotspotSystem. |

### Location Option

| Action | Method | Description |
| --- | --- | --- |
| [List Location Options](actions/list-location-options.md) | GET | Retrieves the resource owner's locations as options from HotspotSystem. |

### Mac Transaction

| Action | Method | Description |
| --- | --- | --- |
| [List MAC Transactions](actions/list-mac-transactions.md) | GET | Retrieves the resource owner's MAC transactions from HotspotSystem. |
| [List MAC Transactions by Location](actions/list-mac-transactions-by-location.md) | GET | Retrieves MAC transactions at a specific location from HotspotSystem. |

### Owner

| Action | Method | Description |
| --- | --- | --- |
| [Verify Credentials](actions/verify-credentials.md) | GET | Verifies HotspotSystem credentials and retrieves owner details. |

### Paid Transaction

| Action | Method | Description |
| --- | --- | --- |
| [List Paid Transactions](actions/list-paid-transactions.md) | GET | Retrieves the resource owner's paid transactions from HotspotSystem. |

### Social Transaction

| Action | Method | Description |
| --- | --- | --- |
| [List Social Transactions](actions/list-social-transactions.md) | GET | Retrieves the resource owner's social transactions from HotspotSystem. |
| [List Social Transactions by Location](actions/list-social-transactions-by-location.md) | GET | Retrieves social transactions at a specific location from HotspotSystem. |

### Subscriber

| Action | Method | Description |
| --- | --- | --- |
| [List Subscribers](actions/list-subscribers.md) | GET | Retrieves the resource owner's subscribers from HotspotSystem. |
| [List Subscribers by Location](actions/list-subscribers-by-location.md) | GET | Retrieves subscribers at a specific location from HotspotSystem. |

### Voucher Transaction

| Action | Method | Description |
| --- | --- | --- |
| [List Voucher Transactions](actions/list-voucher-transactions.md) | GET | Retrieves the resource owner's voucher transactions from HotspotSystem. |
| [List Voucher Transactions by Location](actions/list-voucher-transactions-by-location.md) | GET | Retrieves voucher transactions at a specific location from HotspotSystem. |

