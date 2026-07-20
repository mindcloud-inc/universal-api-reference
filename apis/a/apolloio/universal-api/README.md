# <img src="https://images.mindcloud.co/apps/icons/apollo_1777386882721.png" alt="Apollo logo" width="28" height="28"> Apollo: Universal API

Apollo: Find prospects, enrich contacts, and automate sales outreach

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/apolloio/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 22
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.apollo.io
- **Vendor API docs:** https://docs.apollo.io/reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get User Profile Info](actions/get-user-profile-info.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/apolloio/latest/actions/get-user-profile-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (22)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Bulk Create Accounts](actions/bulk-create-accounts.md) | POST | Creates multiple new accounts in Apollo. |
| [Search for Accounts](actions/search-for-accounts.md) | GET | Finds accounts in your Apollo account. |
| [View an Account](actions/view-an-account.md) | GET | Retrieves an account record from Apollo. |

### Contact Stage

| Action | Method | Description |
| --- | --- | --- |
| [List Contact Stages](actions/list-contact-stages.md) | GET | Retrieves available contact stages from Apollo. |

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [Bulk Create Contacts](actions/bulk-create-contacts.md) | POST | Creates multiple new contacts in Apollo. |
| [Bulk Update Contacts](actions/bulk-update-contacts.md) | PUT | Updates multiple existing contacts in Apollo. |
| [Create a Contact](actions/create-a-contact.md) | POST | Creates a new contact in Apollo. |
| [Search for Contacts](actions/search-for-contacts.md) | GET | Finds contacts in your Apollo account. |
| [Update a Contact](actions/update-a-contact.md) | PUT | Updates an existing contact in Apollo. |
| [Update Contact Stage for Multiple Contacts](actions/update-contact-stage-for-multiple-contacts.md) | PUT | Updates contact stages for multiple contacts in Apollo. |

### Custom Field

| Action | Method | Description |
| --- | --- | --- |
| [Create a Custom Field](actions/create-a-custom-field.md) | POST | Creates a new custom field in Apollo. |

### Emails

| Action | Method | Description |
| --- | --- | --- |
| [Get Inboxes](actions/get-a-list-of-email-accounts.md) | GET | Retrieves information about the linked email inboxes that users (your teammates) use under the authenticated account. This endpoint returns… |

### Job Postings

| Action | Method | Description |
| --- | --- | --- |
| [Organization Job Postings](actions/organization-job-postings.md) | GET | Retrieves organization job postings from Apollo. |

### Leads

| Action | Method | Description |
| --- | --- | --- |
| [Bulk People Enrichment](actions/bulk-people-enrichment.md) | GET | Retrieves enriched data for up to 10 people from Apollo. |
| [People Enrichment](actions/people-enrichment.md) | GET | Retrieves enriched data for a person from Apollo. |

### Lists

| Action | Method | Description |
| --- | --- | --- |
| [Get Lists and Tags](actions/get-a-list-of-all-lists-and-tags.md) | GET | Retrieves information about all lists and tags in your Apollo account. This action can be used to check available lists before using the… |

### Organization

| Action | Method | Description |
| --- | --- | --- |
| [Bulk Organization Enrichment](actions/bulk-organization-enrichment.md) | GET | Retrieves enriched data for up to 10 organizations from Apollo. |
| [Get Complete Organization Info](actions/get-complete-organization-info.md) | GET | Retrieves complete organization information from Apollo. |
| [Organization Enrichment](actions/organization-enrichment.md) | GET | Retrieves enriched data for an organization from Apollo. |
| [Organization Search](actions/organization-search.md) | GET | Finds organizations in Apollo by search criteria. |

### Outreach Email

| Action | Method | Description |
| --- | --- | --- |
| [Search for Outreach Emails](actions/search-for-outreach-emails.md) | GET | Finds outreach emails in your Apollo account. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get User Profile Info](actions/get-user-profile-info.md) | GET | Retrieves the authorized user profile from Apollo. |

