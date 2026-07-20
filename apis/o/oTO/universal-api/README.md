# <img src="https://images.mindcloud.co/apps/icons/favicon-13_1775163530366.png" alt="OTO logo" width="28" height="28"> OTO: Universal API

Manage shipping accounts, orders, shipments, and tracking in OTO

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/oTO/latest
- **Category:** Commerce / Supply Chain
- **Actions:** 20
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.tryoto.com/
- **Vendor API docs:** https://help.tryoto.com/en/support/solutions/folders/150000545667

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Account Info](actions/get-account-info.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oTO/latest/actions/get-account-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (20)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Get Account Info](actions/get-account-info.md) | GET | Retrieves account information from the OTO API. |

### Order

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Order](actions/cancel-order.md) | PUT | Cancels an existing order in OTO. |
| [Get Order Details](actions/get-order-details.md) | GET | Retrieves order details from the OTO API. |
| [List Orders](actions/list-orders.md) | GET | Retrieves a list of orders from OTO. |

### Other

| Action | Method | Description |
| --- | --- | --- |
| [Add Box](actions/add-box.md) | POST | Creates a new box in OTO. |
| [Check Coverage](actions/check-coverage.md) | GET | Checks delivery coverage in the OTO API. |
| [Check Delivery Fee](actions/check-delivery-fee.md) | GET | Checks delivery fees in the OTO API. |
| [Check OTO Delivery Fee](actions/check-oto-delivery-fee.md) | GET | Checks OTO delivery fees in the OTO API. |
| [Create Brand](actions/create-brand.md) | POST | Creates a new brand in OTO. |
| [Get Boxes](actions/get-boxes.md) | GET | Retrieves boxes from the OTO API. |
| [Get Client Info](actions/get-client-info.md) | GET | Retrieves client information from the OTO API. |
| [List Available Cities](actions/list-available-cities.md) | GET | Retrieves available cities from the OTO API. |
| [List Available Time Slots](actions/list-available-time-slots.md) | GET | Retrieves available time slots from the OTO API. |
| [List Brands](actions/list-brands.md) | GET | Retrieves brands from the OTO API. |
| [List Cities](actions/list-cities.md) | GET | Retrieves cities from the OTO API. |
| [List Credit Transactions](actions/list-credit-transactions.md) | GET | Retrieves credit transactions from the OTO API. |
| [List Delivery Companies](actions/list-delivery-companies.md) | GET | Retrieves delivery companies from the OTO API. |
| [List Pickup Locations](actions/list-pickup-locations.md) | GET | Retrieves pickup locations from the OTO API. |
| [List Sales Channels](actions/list-sales-channels.md) | GET | Retrieves sales channels from the OTO API. |
| [Update Box](actions/update-box.md) | PUT | Updates an existing box in OTO. |

