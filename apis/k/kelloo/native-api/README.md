# Kelloo: Native API Reference

A consolidated summary of Kelloo's API configuration and 19 documented operations, with links to official documentation.

- **Official docs:** https://documenter.getpostman.com/view/14463756/UzBgtpF8
- **API base URL:** `https://plan.kelloo.com/api`

## Authentication

### OAuth 2.0

Authorize Kelloo with OAuth 2.0 authorization-code flow.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://plan.kelloo.com/oauth2/authorize to approve access.
2. Exchange the returned authorization code with a POST request to https://plan.kelloo.com/OAuth2/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.


The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://plan.kelloo.com/api/Authenticate.

[Official authentication documentation](https://documenter.getpostman.com/view/14463756/UzBgtpF8#authentication)

## Endpoints (19 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get All Products](actions/get-all-products.md) | `GET /Product` | [docs](https://documenter.getpostman.com/view/14463756/UzBgtpF8#8f7f798a-dfc4-45a2-a383-e64e349b4859) |
| [Get All Projects](actions/get-all-projects.md) | `GET /Project` | [docs](https://documenter.getpostman.com/view/14463756/UzBgtpF8#5efd9710-d8df-415b-ba7d-5034f86041b7) |
| [Get All Resources](actions/get-all-resources.md) | `GET /Resource` | [docs](https://documenter.getpostman.com/view/14463756/UzBgtpF8#73e5aa10-3839-45e0-a388-731202e6d954) |
| [Get All Roles](actions/get-all-roles.md) | `GET /Role` | [docs](https://documenter.getpostman.com/view/14463756/UzBgtpF8#81bcfc6e-9ed9-4709-b46c-da799b30bcab) |
| [Get All Scenario Projects](actions/get-all-scenario-projects.md) | `GET /ScenarioProject` | [docs](https://documenter.getpostman.com/view/14463756/UzBgtpF8#06233451-781b-4ed8-8211-50fcb92626b0) |
| [Get All Scenarios](actions/get-all-scenarios.md) | `GET /Scenario` | [docs](https://documenter.getpostman.com/view/14463756/UzBgtpF8#4076ec9c-1231-49c1-a6d0-565b72f360bf) |
| [Get All Teams](actions/get-all-teams.md) | `GET /Team` | [docs](https://documenter.getpostman.com/view/14463756/UzBgtpF8#5691ee11-7b2d-4334-81f3-f85bc7a60263) |
| [Get Application Configuration](actions/get-application-configuration.md) | `GET /ApplicationConfig` | [docs](https://documenter.getpostman.com/view/14463756/UzBgtpF8#50064719-3321-4111-b3d7-303c2fe0fdcc) |
| [Get Product](actions/get-product.md) | `GET /Product` | [docs](https://documenter.getpostman.com/view/14463756/UzBgtpF8#92d7a745-2779-4cf6-a382-f7586d43b0b9) |
| [Get Project](actions/get-project.md) | `GET /Project` | [docs](https://documenter.getpostman.com/view/14463756/UzBgtpF8#6b1c9a18-96a9-4337-bd36-fac7f40ca1b7) |
| [Get Project Lookup Values](actions/get-project-lookup-values.md) | `GET /ProjectLookup` | [docs](https://documenter.getpostman.com/view/14463756/UzBgtpF8#3b6c0e86-fa52-4171-9008-b09112f1b51c) |
| [Get Project Lookups](actions/get-project-lookups.md) | `GET /ProjectLookup` | [docs](https://documenter.getpostman.com/view/14463756/UzBgtpF8#a69c647c-0456-4fa5-9e18-0693c01c88ba) |
| [Get Resource](actions/get-resource.md) | `GET /Resource` | [docs](https://documenter.getpostman.com/view/14463756/UzBgtpF8#4ad85043-cdfb-48e8-926e-12fc1d5f00d3) |
| [Get Role](actions/get-role.md) | `GET /Role` | [docs](https://documenter.getpostman.com/view/14463756/UzBgtpF8#c3075640-9b02-48ba-83a3-1eb7bc0e3f5b) |
| [Get Scenario](actions/get-scenario.md) | `GET /Scenario` | [docs](https://documenter.getpostman.com/view/14463756/UzBgtpF8#96ad5405-feea-4916-a048-35f522a81115) |
| [Get Team](actions/get-team.md) | `GET /Team` | [docs](https://documenter.getpostman.com/view/14463756/UzBgtpF8#7278fd36-4489-4d1f-95c1-9d31626b97b0) |
| [Get Work Item](actions/get-work-item.md) | `GET /WorkItem` | [docs](https://documenter.getpostman.com/view/14463756/UzBgtpF8#d4820d69-cce1-4c02-a5a4-cd70f7dfff81) |
| [Get Work Item Segments](actions/get-work-item-segments.md) | `GET /WorkSegment` | [docs](https://documenter.getpostman.com/view/14463756/UzBgtpF8#f99f241a-c448-4033-9547-744effb257bc) |
| [Get Work Items](actions/get-work-items.md) | `GET /WorkItem` | [docs](https://documenter.getpostman.com/view/14463756/UzBgtpF8#1c287bc7-c331-4281-8f14-0931483bd577) |
