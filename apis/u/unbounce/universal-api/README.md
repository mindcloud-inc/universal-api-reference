# <img src="https://images.mindcloud.co/apps/icons/unbounce-logo-png-transparent_1772724485745.png" alt="Unbounce logo" width="28" height="28"> Unbounce: Universal API

Build landing pages, launch popups, run tests, and optimize conversions.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/unbounce/latest
- **Category:** Marketing
- **Actions:** 18
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://unbounce.com
- **Vendor API docs:** https://developer.unbounce.com/api_reference/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Accounts](actions/list-accounts.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/unbounce/latest/actions/list-accounts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (18)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [List Accounts](actions/list-accounts.md) | GET | Retrieves the accounts collection from Unbounce. |
| [Retrieve Account](actions/retrieve-account.md) | GET | Retrieves details for an Unbounce account. |

### Form Field

| Action | Method | Description |
| --- | --- | --- |
| [List Page Form Fields](actions/list-page-form-fields.md) | GET | Retrieves form fields across all variants of an Unbounce page. |

### Lead

| Action | Method | Description |
| --- | --- | --- |
| [Create Page Lead](actions/create-page-lead.md) | POST | Creates a lead for an Unbounce page. |
| [Delete Page Lead](actions/delete-page-lead.md) | DELETE | Deletes a specific lead from an Unbounce page. |
| [Get Lead](actions/get-lead.md) | GET | Retrieves a specific lead from Unbounce. |
| [Get Page Lead](actions/get-page-lead.md) | GET | Retrieves a specific lead from an Unbounce page. |
| [List Page Leads](actions/list-page-leads.md) | GET | Retrieves leads for an Unbounce page. |

### Lead Deletion Request

| Action | Method | Description |
| --- | --- | --- |
| [Create Lead Deletion Request](actions/create-lead-deletion-request.md) | POST | Creates an asynchronous lead deletion request in Unbounce. |
| [Retrieve Lead Deletion Request](actions/retrieve-lead-deletion-request.md) | GET | Retrieves a lead deletion request from Unbounce. |

### Page

| Action | Method | Description |
| --- | --- | --- |
| [List Account Pages](actions/list-account-pages.md) | GET | Retrieves pages for a specified Unbounce account. |
| [List Page Group Pages](actions/list-page-group-pages.md) | GET | Retrieves pages for an Unbounce page group. |
| [List Pages](actions/list-pages.md) | GET | Retrieves all accessible pages from Unbounce. |
| [List Sub Account Pages](actions/list-sub-account-pages.md) | GET | Retrieves pages for an Unbounce sub-account. |
| [Retrieve Page](actions/retrieve-page.md) | GET | Retrieves details for an Unbounce page. |

### Page Group

| Action | Method | Description |
| --- | --- | --- |
| [List Sub Account Page Groups](actions/list-sub-account-page-groups.md) | GET | Retrieves page groups for an Unbounce sub-account. |

### Sub Account

| Action | Method | Description |
| --- | --- | --- |
| [List Account Sub Accounts](actions/list-account-sub-accounts.md) | GET | Retrieves sub-accounts for a specified Unbounce account. |
| [Retrieve Sub Account](actions/retrieve-sub-account.md) | GET | Retrieves details for an Unbounce sub-account. |

