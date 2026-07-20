# OTO: Native API Reference

A consolidated summary of OTO's API configuration and 20 documented operations, with links to official documentation.

- **Official docs:** https://help.tryoto.com/en/support/solutions/folders/150000545667
- **API base URL:** `https://api.tryoto.com/rest/v2`

## Authentication

### Refresh Token

Exchange an OTO refresh token for a temporary bearer access token using the documented refreshToken endpoint.

### Credentials

- **Refresh Token:** `refreshToken` · required · Permanent OTO refresh token from Settings -> API Integrations.

Send these headers with each API request:

```http
Authorization: Bearer <custom.access_token>
```

[Official authentication documentation](https://help.tryoto.com/en/support/solutions/articles/150000213805-authorization)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (20 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Box](actions/add-box.md) | `POST /addBox` | [docs](https://help.tryoto.com/en/support/solutions/articles/150000213809-shipments-apis) |
| [Cancel Order](actions/cancel-order.md) | `POST /cancelOrder` | [docs](https://help.tryoto.com/en/support/solutions/articles/150000213808-orders-apis) |
| [Check Coverage](actions/check-coverage.md) | `POST /checkCoverage` | [docs](https://help.tryoto.com/en/support/solutions/articles/150000213813-carrier-integrations-apis) |
| [Check Delivery Fee](actions/check-delivery-fee.md) | `POST /checkDeliveryFee` | [docs](https://help.tryoto.com/en/support/solutions/articles/150000213813-carrier-integrations-apis) |
| [Check OTO Delivery Fee](actions/check-oto-delivery-fee.md) | `POST /checkOTODeliveryFee` | [docs](https://help.tryoto.com/en/support/solutions/articles/150000213820-oto-flex-apis) |
| [Create Brand](actions/create-brand.md) | `POST /createBrand` | [docs](https://help.tryoto.com/en/support/solutions/articles/150000213815-brands-apis) |
| [Get Account Info](actions/get-account-info.md) | `GET /accountInfo` | [docs](https://help.tryoto.com/en/support/solutions/articles/150000213806-account-apis) |
| [Get Boxes](actions/get-boxes.md) | `GET /getBox` | [docs](https://help.tryoto.com/en/support/solutions/articles/150000213809-shipments-apis) |
| [Get Client Info](actions/get-client-info.md) | `GET /clientInfo` | [docs](https://help.tryoto.com/en/support/solutions/articles/150000213806-account-apis) |
| [Get Order Details](actions/get-order-details.md) | `GET /orderDetails` | [docs](https://help.tryoto.com/en/support/solutions/articles/150000213808-orders-apis) |
| [List Available Cities](actions/list-available-cities.md) | `POST /availableCities` | [docs](https://help.tryoto.com/en/support/solutions/articles/150000213813-carrier-integrations-apis) |
| [List Available Time Slots](actions/list-available-time-slots.md) | `POST /availableTimeslots` | [docs](https://help.tryoto.com/en/support/solutions/articles/150000213813-carrier-integrations-apis) |
| [List Brands](actions/list-brands.md) | `GET /getBrandList` | [docs](https://help.tryoto.com/en/support/solutions/articles/150000213815-brands-apis) |
| [List Cities](actions/list-cities.md) | `POST /getCities` | [docs](https://help.tryoto.com/en/support/solutions/articles/150000213813-carrier-integrations-apis) |
| [List Credit Transactions](actions/list-credit-transactions.md) | `GET /creditTransactions` | [docs](https://help.tryoto.com/en/support/solutions/articles/150000213809-shipments-apis) |
| [List Delivery Companies](actions/list-delivery-companies.md) | `POST /dcList` | [docs](https://help.tryoto.com/en/support/solutions/articles/150000213813-carrier-integrations-apis) |
| [List Orders](actions/list-orders.md) | `GET /orders` | [docs](https://help.tryoto.com/en/support/solutions/articles/150000213808-orders-apis) |
| [List Pickup Locations](actions/list-pickup-locations.md) | `GET /getPickupLocationList` | [docs](https://help.tryoto.com/en/support/solutions/articles/150000213814-pickup-locations) |
| [List Sales Channels](actions/list-sales-channels.md) | `GET /salesChannel/getSalesChannelsList` | [docs](https://help.tryoto.com/en/support/solutions/articles/150000213816-sales-channels-apis) |
| [Update Box](actions/update-box.md) | `POST /updateBox` | [docs](https://help.tryoto.com/en/support/solutions/articles/150000213809-shipments-apis) |
