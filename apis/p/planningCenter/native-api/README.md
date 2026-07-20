# Planning Center: Native API Reference

A consolidated summary of Planning Center's API configuration and 23 documented operations, with links to official documentation.

- **Official docs:** https://api.planningcenteronline.com/docs/apps
- **API base URL:** `https://api.planningcenteronline.com`

## Authentication

### OAuth 2.0

Connect a Planning Center account with OAuth 2.0.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://api.planningcenteronline.com/oauth/authorize to approve access.
2. Exchange the returned authorization code with a POST request to https://api.planningcenteronline.com/oauth/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `api calendar check_ins giving groups people publishing registrations services`.

PKCE is enabled with the `other` challenge method. The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://api.planningcenteronline.com/oauth/token.

[Official authentication documentation](https://api.planningcenteronline.com/docs/overview/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `data`.

## Pagination

Use `per_page` in the query string to set the page size (default 25; accepted range 1–100). Use `offset` in the query string as the record offset; numbering starts at 0.

## Endpoints (23 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Household](actions/create-household.md) | `POST /people/v2/households` | [docs](https://api.planningcenteronline.com/docs/apps/people/versions/2025-11-10/vertices/household) |
| [Create Household Membership](actions/create-household-membership.md) | `POST /people/v2/households/:household_id/household_memberships` | [docs](https://api.planningcenteronline.com/docs/apps/people/versions/2025-11-10/vertices/household_membership) |
| [Create Person](actions/create-person.md) | `POST /people/v2/people` | [docs](https://api.planningcenteronline.com/docs/apps/people/versions/2025-11-10/vertices/person) |
| [Get Household](actions/get-household.md) | `GET /people/v2/households/:id` | [docs](https://api.planningcenteronline.com/docs/apps/people/versions/2025-11-10/vertices/household) |
| [Get List](actions/get-list.md) | `GET /people/v2/lists/:id` | [docs](https://api.planningcenteronline.com/docs/apps/people/versions/2025-11-10/vertices/list) |
| [Get Person](actions/get-person.md) | `GET /people/v2/people/:id` | [docs](https://api.planningcenteronline.com/docs/apps/people/versions/2025-11-10/vertices/person) |
| [Get Workflow](actions/get-workflow.md) | `GET /people/v2/workflows/:id` | [docs](https://api.planningcenteronline.com/docs/apps/people/versions/2025-11-10/vertices/workflow) |
| [List Campuses](actions/list-campuses.md) | `GET /people/v2/campuses` | [docs](https://api.planningcenteronline.com/docs/apps/people/versions/2025-11-10/vertices/campus) |
| [List Household People](actions/list-household-people.md) | `GET /people/v2/households/:household_id/people` | [docs](https://api.planningcenteronline.com/docs/apps/people/versions/2025-11-10/vertices/household) |
| [List Households](actions/list-households.md) | `GET /people/v2/households` | [docs](https://api.planningcenteronline.com/docs/apps/people/versions/2025-11-10/vertices/household) |
| [List List Results](actions/list-list-results.md) | `GET /people/v2/lists/:list_id/list_results` | [docs](https://api.planningcenteronline.com/docs/apps/people/versions/2025-11-10/vertices/list_result) |
| [List Lists](actions/list-lists.md) | `GET /people/v2/lists` | [docs](https://api.planningcenteronline.com/docs/apps/people/versions/2025-11-10/vertices/list) |
| [List People](actions/list-people.md) | `GET /people/v2/people` | [docs](https://api.planningcenteronline.com/docs/apps/people/versions/2025-11-10/vertices/person) |
| [List Person Addresses](actions/list-person-addresses.md) | `GET /people/v2/people/:person_id/addresses` | [docs](https://api.planningcenteronline.com/docs/apps/people/versions/2025-11-10/vertices/address) |
| [List Person Emails](actions/list-person-emails.md) | `GET /people/v2/people/:person_id/emails` | [docs](https://api.planningcenteronline.com/docs/apps/people/versions/2025-11-10/vertices/email) |
| [List Person Field Data](actions/list-person-field-data.md) | `GET /people/v2/people/:person_id/field_data` | [docs](https://api.planningcenteronline.com/docs/apps/people/versions/2025-11-10/vertices/person) |
| [List Person Households](actions/list-person-households.md) | `GET /people/v2/people/:person_id/households` | [docs](https://api.planningcenteronline.com/docs/apps/people/versions/2025-11-10/vertices/person) |
| [List Person Notes](actions/list-person-notes.md) | `GET /people/v2/people/:person_id/notes` | [docs](https://api.planningcenteronline.com/docs/apps/people/versions/2025-11-10/vertices/note) |
| [List Person Phone Numbers](actions/list-person-phone-numbers.md) | `GET /people/v2/people/:person_id/phone_numbers` | [docs](https://api.planningcenteronline.com/docs/apps/people/versions/2025-11-10/vertices/phone_number) |
| [List Workflow Cards](actions/list-workflow-cards.md) | `GET /people/v2/people/:person_id/workflow_cards` | [docs](https://api.planningcenteronline.com/docs/apps/people/versions/2025-11-10/vertices/workflow_card) |
| [List Workflows](actions/list-workflows.md) | `GET /people/v2/workflows` | [docs](https://api.planningcenteronline.com/docs/apps/people/versions/2025-11-10/vertices/workflow) |
| [Update Household](actions/update-household.md) | `PATCH /people/v2/households/:id` | [docs](https://api.planningcenteronline.com/docs/apps/people/versions/2025-11-10/vertices/household) |
| [Update Person](actions/update-person.md) | `PATCH /people/v2/people/:id` | [docs](https://api.planningcenteronline.com/docs/apps/people/versions/2025-11-10/vertices/person) |
