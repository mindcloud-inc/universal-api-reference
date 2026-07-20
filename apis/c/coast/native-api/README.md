# Coast: Native API Reference

A consolidated summary of Coast's API configuration and 42 documented operations, with links to official documentation.

- **Official docs:** https://coastpay.com/integrations/
- **API base URL:** `https://public.coastpay.com`

## Authentication

### API Key

Use a Coast API key from the Coast portal to authenticate requests.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://coastpay.com/integrations/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. The next-page cursor is read from `nextPageToken`.

## Pagination

Use `pageSize` in the query string to set the page size (default 10; accepted range 1–100). Use `nextPageToken` in the query string as the pagination cursor.

## Endpoints (42 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Department](actions/createdepartment.md) | `POST /v2/departments` | [docs](https://coastpay.com/integrations/) |
| [Create Location](actions/createlocation.md) | `POST /v2/locations` | [docs](https://coastpay.com/integrations/) |
| [Create Person](actions/createperson.md) | `POST /v2/people` | [docs](https://coastpay.com/integrations/) |
| [Create Policy](actions/createpolicy.md) | `POST /v2/policies` | [docs](https://coastpay.com/integrations/) |
| [Create Role](actions/createrole.md) | `POST /v2/roles` | [docs](https://coastpay.com/integrations/) |
| [Create Vehicle](actions/createvehicle.md) | `POST /v2/vehicles` | [docs](https://coastpay.com/integrations/) |
| [Delete Department By ID](actions/deletedepartment.md) | `DELETE /v2/departments/:departmentId` | [docs](https://coastpay.com/integrations/) |
| [Delete Location By ID](actions/deletelocation.md) | `DELETE /v2/locations/:locationId` | [docs](https://coastpay.com/integrations/) |
| [Get Card By ID](actions/getcard.md) | `GET /v2/cards/:cardId` | [docs](https://coastpay.com/integrations/) |
| [Get All Cards](actions/getcards.md) | `GET /v2/cards` | [docs](https://coastpay.com/integrations/) |
| [Get Department By ID](actions/getdepartment.md) | `GET /v2/departments/:departmentId` | [docs](https://coastpay.com/integrations/) |
| [Get All Departments](actions/getdepartments.md) | `GET /v2/departments` | [docs](https://coastpay.com/integrations/) |
| [Get Location By ID](actions/getlocation.md) | `GET /v2/locations/:locationId` | [docs](https://coastpay.com/integrations/) |
| [Get All Locations](actions/getlocations.md) | `GET /v2/locations` | [docs](https://coastpay.com/integrations/) |
| [Get My Account](actions/getmyaccount.md) | `GET /v2/account` | [docs](https://coastpay.com/integrations/) |
| [Get All People](actions/getpeople.md) | `GET /v2/people` | [docs](https://coastpay.com/integrations/) |
| [Get Person By ID](actions/getperson.md) | `GET /v2/people/:personId` | [docs](https://coastpay.com/integrations/) |
| [Get All Policies](actions/getpolicies.md) | `GET /v2/policies` | [docs](https://coastpay.com/integrations/) |
| [Get Policy By ID](actions/getpolicy.md) | `GET /v2/policies/:policyId` | [docs](https://coastpay.com/integrations/) |
| [Get Purchase By ID](actions/getpurchase.md) | `GET /v2/transactions/purchases/:purchaseId` | [docs](https://coastpay.com/integrations/) |
| [Get All Purchases](actions/getpurchases.md) | `GET /v2/transactions/purchases` | [docs](https://coastpay.com/integrations/) |
| [Get Role By ID](actions/getrole.md) | `GET /v2/roles/:roleId` | [docs](https://coastpay.com/integrations/) |
| [Get All Roles](actions/getroles.md) | `GET /v2/roles` | [docs](https://coastpay.com/integrations/) |
| [Get Vehicle By ID](actions/getvehicle.md) | `GET /v2/vehicles/:vehicleId` | [docs](https://coastpay.com/integrations/) |
| [Get All Vehicles](actions/getvehicles.md) | `GET /v2/vehicles` | [docs](https://coastpay.com/integrations/) |
| [Order Everyday Purchase Virtual Card](actions/ordereverydaypurchasevirtualcard.md) | `POST /v2/cards/virtual` | [docs](https://coastpay.com/integrations/) |
| [Order Project Virtual Card](actions/orderprojectvirtualcard.md) | `POST /v2/cards/virtual` | [docs](https://coastpay.com/integrations/) |
| [Order Subscription Virtual Card](actions/ordersubscriptionvirtualcard.md) | `POST /v2/cards/virtual` | [docs](https://coastpay.com/integrations/) |
| [Update Department By ID](actions/updatedepartment.md) | `PATCH /v2/departments/:departmentId` | [docs](https://coastpay.com/integrations/) |
| [Update Everyday Purchase Card By ID](actions/updateeverydaypurchasecardbyid.md) | `PATCH /v2/cards/:cardId` | [docs](https://coastpay.com/integrations/) |
| [Update Fleet Card By ID](actions/updatefleetcardbyid.md) | `PATCH /v2/cards/:cardId` | [docs](https://coastpay.com/integrations/) |
| [Update Location By ID](actions/updatelocation.md) | `PATCH /v2/locations/:locationId` | [docs](https://coastpay.com/integrations/) |
| [Update My Account Settings](actions/updatemyaccountsettings.md) | `PATCH /v2/account/settings` | [docs](https://coastpay.com/integrations/) |
| [Update Person By ID](actions/updateperson.md) | `PATCH /v2/people/:personId` | [docs](https://coastpay.com/integrations/) |
| [Update Personalized Card By ID](actions/updatepersonalizedcardbyid.md) | `PATCH /v2/cards/:cardId` | [docs](https://coastpay.com/integrations/) |
| [Update Policy By ID](actions/updatepolicy.md) | `PUT /v2/policies/:policyId` | [docs](https://coastpay.com/integrations/) |
| [Update Project Card By ID](actions/updateprojectcardbyid.md) | `PATCH /v2/cards/:cardId` | [docs](https://coastpay.com/integrations/) |
| [Update Role By ID](actions/updaterole.md) | `PATCH /v2/roles/:roleId` | [docs](https://coastpay.com/integrations/) |
| [Update Subscription Card By ID](actions/updatesubscriptioncardbyid.md) | `PATCH /v2/cards/:cardId` | [docs](https://coastpay.com/integrations/) |
| [Update Vehicle By ID](actions/updatevehicle.md) | `PATCH /v2/vehicles/:vehicleId` | [docs](https://coastpay.com/integrations/) |
| [Update Vehicle PIN Card By ID](actions/updatevehiclepincardbyid.md) | `PATCH /v2/cards/:cardId` | [docs](https://coastpay.com/integrations/) |
| [Update Vehicle Stats](actions/updatevehiclestats.md) | `POST /v2/vehicles/telematics` | [docs](https://coastpay.com/integrations/) |
