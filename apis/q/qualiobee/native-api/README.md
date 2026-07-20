# Qualiobee: Native API Reference

A consolidated summary of Qualiobee's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://app.qualiobee.fr/api/doc/
- **API base URL:** `https://app.qualiobee.fr/api`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required · Your Qualiobee API key from Paramètres organisation > Connexions externes

Send these headers with each API request:

```http
x-api-key: <apiKey>
```

[Official authentication documentation](https://app.qualiobee.fr/api/doc/)

## API conventions

Response data is read from `data`. The total page count is read from `pageCount`. The current page number is read from `page`.

## Pagination

Use `limit` in the query string to set the page size (default 5; minimum 1). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Customer](actions/create-customer.md) | `POST /:organizationUuid/customer` | [docs](https://app.qualiobee.fr/api/doc/#/Customer/PublicCustomerController_createOne) |
| [Create Formation](actions/create-formation.md) | `POST /:organizationUuid/formation` | [docs](https://app.qualiobee.fr/api/doc/#/Formation/PublicFormationController_createOne) |
| [Create Learner](actions/create-learner.md) | `POST /:organizationUuid/learner` | [docs](https://app.qualiobee.fr/api/doc/#/Learner/PublicLearnerController_createOne) |
| [Create Location](actions/create-location.md) | `POST /:organizationUuid/location` | [docs](https://app.qualiobee.fr/api/doc/#/Location/PublicLocationController_createOne) |
| [Create Session](actions/create-session.md) | `POST /:organizationUuid/session` | [docs](https://app.qualiobee.fr/api/doc/#/Session/PublicSessionController_createOne) |
| [Get Convention](actions/get-convention.md) | `GET /:organizationUuid/convention/:conventionUuid` | [docs](https://app.qualiobee.fr/api/doc/#/Convention/PublicConventionController_getOne) |
| [Get Customer](actions/get-customer.md) | `GET /:organizationUuid/customer/:customerUuid` | [docs](https://app.qualiobee.fr/api/doc/#/Customer/PublicCustomerController_getOne) |
| [Get Formation](actions/get-formation.md) | `GET /:organizationUuid/formation/:formationUuid` | [docs](https://app.qualiobee.fr/api/doc/#/Formation/PublicFormationController_getOne) |
| [Get Learner](actions/get-learner.md) | `GET /:organizationUuid/learner/:learnerUuid` | [docs](https://app.qualiobee.fr/api/doc/#/Learner/PublicLearnerController_getOne) |
| [Get Location](actions/get-location.md) | `GET /:organizationUuid/location/:locationUuid` | [docs](https://app.qualiobee.fr/api/doc/#/Location/PublicLocationController_getOne) |
| [Get Qualiobee Account](actions/get-qualiobee-account.md) | `GET /:organizationUuid/qualiobee/:qualiobeeUuid` | [docs](https://app.qualiobee.fr/api/doc/#/Qualiobee/PublicQualiobeeController_getOne) |
| [Get Session](actions/get-session.md) | `GET /:organizationUuid/session/:sessionUuid` | [docs](https://app.qualiobee.fr/api/doc/#/Session/PublicSessionController_getOne) |
| [List Conventions](actions/list-conventions.md) | `GET /:organizationUuid/convention` | [docs](https://app.qualiobee.fr/api/doc/#/Convention/PublicConventionController_getMany) |
| [List Customers](actions/list-customers.md) | `GET /:organizationUuid/customer` | [docs](https://app.qualiobee.fr/api/doc/#/Customer/PublicCustomerController_getMany) |
| [List Formations](actions/list-formations.md) | `GET /:organizationUuid/formation` | [docs](https://app.qualiobee.fr/api/doc/#/Formation/PublicFormationController_getMany) |
| [List Learners](actions/list-learners.md) | `GET /:organizationUuid/learner` | [docs](https://app.qualiobee.fr/api/doc/#/Learner/PublicLearnerController_getMany) |
| [List Locations](actions/list-locations.md) | `GET /:organizationUuid/location` | [docs](https://app.qualiobee.fr/api/doc/#/Location/PublicLocationController_getMany) |
| [List Sessions](actions/list-sessions.md) | `GET /:organizationUuid/session` | [docs](https://app.qualiobee.fr/api/doc/#/Session/PublicSessionController_getMany) |
| [Start Session](actions/start-session.md) | `PATCH /:organizationUuid/session/:sessionUuid/go` | [docs](https://app.qualiobee.fr/api/doc/#/Session/PublicSessionController_go) |
| [Update Customer](actions/update-customer.md) | `PATCH /:organizationUuid/customer/:customerUuid` | [docs](https://app.qualiobee.fr/api/doc/#/Customer/PublicCustomerController_updateOne) |
| [Update Formation](actions/update-formation.md) | `PATCH /:organizationUuid/formation/:formationUuid` | [docs](https://app.qualiobee.fr/api/doc/#/Formation/PublicFormationController_updateOne) |
| [Update Learner](actions/update-learner.md) | `PATCH /:organizationUuid/learner/:learnerUuid` | [docs](https://app.qualiobee.fr/api/doc/#/Learner/PublicLearnerController_updateOne) |
| [Update Location](actions/update-location.md) | `PATCH /:organizationUuid/location/:locationUuid` | [docs](https://app.qualiobee.fr/api/doc/#/Location/PublicLocationController_updateOne) |
| [Update Session](actions/update-session.md) | `PATCH /:organizationUuid/session/:sessionUuid` | [docs](https://app.qualiobee.fr/api/doc/#/Session/PublicSessionController_updateOne) |
