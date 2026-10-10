# Apollo: Native API Reference

A consolidated summary of Apollo's API configuration and 25 documented operations, with links to official documentation.

- **Official docs:** https://docs.apollo.io/reference
- **API base URL:** `https://app.apollo.io/api`

## Authentication

### OAuth 2.0

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://app.apollo.io/#/oauth/authorize to approve access.
2. Exchange the returned authorization code with a POST request to https://app.apollo.io/api/v1/oauth/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `read_user_profile app_scopes people_bulk_match organizations_bulk_enrich organizations_enrich people_match organizations_job_posting mixed_companies_search organizations_search organization_read person_read mixed_people_organization_top_people mixed_people_api_search opportunity_write opportunities_list opportunity_read opportunity_update contact_write contact_update contacts_bulk_create contacts_bulk_update contacts_search contact_stages_list contact_stages_update contact_owners_update contact_read account_write account_bulk_create account_update accounts_search account_stages_list account_stages_update account_owners_update account_read emailer_campaigns_search emailer_campaigns_add_contact_ids emailer_campaigns_remove_or_stop_contact_ids emailer_messages_search tasks_create tasks_list users_list email_accounts_list tags_list custom_fields_list custom_field_write opportunity_stages_list report_sync lists_add_entities`.

The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://app.apollo.io/api/v1/oauth/token.

[Official authentication documentation](https://docs.apollo.io/docs/use-oauth-20-authorization-flow-to-access-apollo-user-information-partners)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json; charset=utf-8` |

## Endpoints (25 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Records to a List](actions/add-records-to-a-list.md) | `POST v1/labels/add_entity_ids_to_label_names` | [docs](https://docs.apollo.io/reference/add-records-to-a-list) |
| [Bulk Create Accounts](actions/bulk-create-accounts.md) | `POST v1/accounts/bulk_create` | [docs](https://docs.apollo.io/reference/bulk-create-accounts) |
| [Bulk Create Contacts](actions/bulk-create-contacts.md) | `POST v1/contacts/bulk_create` | [docs](https://docs.apollo.io/reference/bulk-create-contacts) |
| [Bulk Organization Enrichment](actions/bulk-organization-enrichment.md) | `POST v1/organizations/bulk_enrich` | [docs](https://docs.apollo.io/reference/bulk-organization-enrichment) |
| [Bulk People Enrichment](actions/bulk-people-enrichment.md) | `POST v1/people/bulk_match` | [docs](https://docs.apollo.io/reference/bulk-people-enrichment) |
| [Bulk Update Contacts](actions/bulk-update-contacts.md) | `POST v1/contacts/bulk_update` | [docs](https://docs.apollo.io/reference/bulk-update-contacts) |
| [Create a Contact](actions/create-a-contact.md) | `POST v1/contacts` | [docs](https://docs.apollo.io/reference/create-a-contact) |
| [Create a Custom Field](actions/create-a-custom-field.md) | `POST v1/fields` | [docs](https://docs.apollo.io/reference/create-a-custom-field) |
| [Get Lists and Tags](actions/get-a-list-of-all-lists-and-tags.md) | `GET v1/labels` | [docs](https://docs.apollo.io/reference/get-a-list-of-all-lists) |
| [Get Inboxes](actions/get-a-list-of-email-accounts.md) | `GET v1/email_accounts` | [docs](https://docs.apollo.io/reference/get-a-list-of-email-accounts) |
| [Get Complete Organization Info](actions/get-complete-organization-info.md) | `GET v1/organizations/:id` | [docs](https://docs.apollo.io/reference/get-complete-organization-info) |
| [Get User Profile Info](actions/get-user-profile-info.md) | `GET v1/users/api_profile` | [docs](https://docs.apollo.io/docs/use-oauth-20-authorization-flow-to-access-apollo-user-information-partners#get-user-profile-info) |
| [List Account Stages](actions/list-account-stages.md) | `GET v1/account_stages` | [docs](https://docs.apollo.io/reference/list-account-stages) |
| [List Contact Stages](actions/list-contact-stages.md) | `GET v1/contact_stages` | [docs](https://docs.apollo.io/reference/list-contact-stages) |
| [Organization Enrichment](actions/organization-enrichment.md) | `GET v1/organizations/enrich` | [docs](https://docs.apollo.io/reference/organization-enrichment) |
| [Organization Job Postings](actions/organization-job-postings.md) | `GET v1/organizations/:organization_id/job_postings` | [docs](https://docs.apollo.io/reference/organization-jobs-postings) |
| [Organization Search](actions/organization-search.md) | `POST v1/mixed_companies/search` | [docs](https://docs.apollo.io/reference/organization-search) |
| [People API Search](actions/people-api-search.md) | `POST v1/mixed_people/api_search` | [docs](https://docs.apollo.io/reference/people-api-search) |
| [People Enrichment](actions/people-enrichment.md) | `POST v1/people/match` | [docs](https://docs.apollo.io/reference/people-enrichment) |
| [Search for Accounts](actions/search-for-accounts.md) | `POST v1/accounts/search` | [docs](https://docs.apollo.io/reference/search-for-accounts) |
| [Search for Contacts](actions/search-for-contacts.md) | `POST v1/contacts/search` | [docs](https://docs.apollo.io/reference/search-for-contacts) |
| [Search for Outreach Emails](actions/search-for-outreach-emails.md) | `GET v1/emailer_messages/search` | [docs](https://docs.apollo.io/reference/search-for-outreach-emails) |
| [Update a Contact](actions/update-a-contact.md) | `PATCH v1/contacts/:contact_id` | [docs](https://docs.apollo.io/reference/update-a-contact) |
| [Update Contact Stage for Multiple Contacts](actions/update-contact-stage-for-multiple-contacts.md) | `POST v1/contacts/update_stages` | [docs](https://docs.apollo.io/reference/update-contact-stage) |
| [View an Account](actions/view-an-account.md) | `GET v1/accounts/:id` | [docs](https://docs.apollo.io/reference/view-an-account) |
