# <img src="https://images.mindcloud.co/apps/icons/microsoft-dynamics365sales_1792675584525.png" alt="Microsoft Dynamics 365 Sales logo" width="28" height="28"> Microsoft Dynamics 365 Sales: Universal API

Manage leads, opportunities, accounts, contacts, and sales records in Microsoft Dynamics 365 Sales.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/microsoftDynamics365Sales/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 20
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.microsoft.com/en-us/dynamics-365/products/sales
- **Vendor API docs:** https://learn.microsoft.com/en-us/dynamics365/sales/developer/developer-guide

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current User](actions/get-current-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/microsoftDynamics365Sales/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (20)

### Accounts

| Action | Method | Description |
| --- | --- | --- |
| [Get Account](actions/get-account.md) | GET |  |
| [List Accounts](actions/list-accounts.md) | GET |  |
| [Update Account](actions/update-account.md) | PUT |  |

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [Get Contact](actions/get-contact.md) | GET |  |
| [List Contacts](actions/list-contacts.md) | GET |  |
| [Update Contact](actions/update-contact.md) | PUT |  |

### Custom Records

| Action | Method | Description |
| --- | --- | --- |
| [Get Custom Record](actions/get-custom-record.md) | GET |  |
| [List Custom Records](actions/list-custom-records.md) | GET |  |
| [Update Custom Record](actions/update-custom-record.md) | PUT |  |

### Leads

| Action | Method | Description |
| --- | --- | --- |
| [Get Lead](actions/get-lead.md) | GET |  |
| [List Leads](actions/list-leads.md) | GET |  |
| [Update Lead](actions/update-lead.md) | PUT |  |

### Opportunities

| Action | Method | Description |
| --- | --- | --- |
| [Get Opportunity](actions/get-opportunity.md) | GET |  |
| [List Opportunities](actions/list-opportunities.md) | GET |  |
| [Update Opportunity](actions/update-opportunity.md) | PUT |  |

### Table Definitions

| Action | Method | Description |
| --- | --- | --- |
| [Get Table Definition](actions/get-table-definition.md) | GET |  |
| [List Table Columns](actions/list-table-columns.md) | GET |  |
| [List Tables](actions/list-tables.md) | GET |  |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | GET |  |
| [List Users](actions/list-users.md) | GET |  |

