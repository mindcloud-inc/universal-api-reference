# <img src="https://images.mindcloud.co/apps/icons/favicon-8_1775075764396.png" alt="NextLead logo" width="28" height="28"> NextLead: Universal API

Simple CRM for contact management, marketing campaigns, sales pipelines, and automations.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/nextLead/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 16
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://nextlead.app/
- **Vendor API docs:** https://dashboard.nextlead.app/en/api-documentation

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Identify Organization](actions/identify-organization.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nextLead/latest/actions/identify-organization?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (16)

### Action

| Action | Method | Description |
| --- | --- | --- |
| [Create Action](actions/create-action.md) | POST | Creates a new task in NextLead. |

### Action Column

| Action | Method | Description |
| --- | --- | --- |
| [List Action Columns](actions/list-action-columns.md) | GET | Retrieves action stage columns from NextLead. |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Find Contact](actions/find-contact.md) | GET | Finds a contact in NextLead by email or LinkedIn. |

### Conversion Status

| Action | Method | Description |
| --- | --- | --- |
| [List Conversion Statuses](actions/list-conversion-statuses.md) | GET | Retrieves available conversion statuses from NextLead. |

### Custom Field

| Action | Method | Description |
| --- | --- | --- |
| [List Custom Fields](actions/list-custom-fields.md) | GET | Retrieves available contact custom fields from NextLead. |

### Form

| Action | Method | Description |
| --- | --- | --- |
| [Create Form](actions/create-form.md) | POST | Creates a new audience list form in NextLead. |
| [Get Form](actions/get-form.md) | GET | Retrieves a form from NextLead by list ID. |

### List

| Action | Method | Description |
| --- | --- | --- |
| [List Lists](actions/list-lists.md) | GET | Retrieves audience lists with details from NextLead. |

### Organization

| Action | Method | Description |
| --- | --- | --- |
| [Identify Organization](actions/identify-organization.md) | GET | Verifies your API key and retrieves your NextLead organization. |

### Sale

| Action | Method | Description |
| --- | --- | --- |
| [Create Sale](actions/create-sale.md) | POST | Creates a new sales deal in NextLead. |

### Sales Column

| Action | Method | Description |
| --- | --- | --- |
| [List Sales Columns](actions/list-sales-columns.md) | GET | Retrieves sales stage columns from NextLead. |

### Structure

| Action | Method | Description |
| --- | --- | --- |
| [Create Structure](actions/create-structure.md) | POST | Creates a new structure in NextLead. |
| [Delete Structure](actions/delete-structure.md) | DELETE | Deletes an existing structure from NextLead. |
| [Edit Structure](actions/edit-structure.md) | PUT | Updates an existing structure in NextLead. |
| [List Structures](actions/list-structures.md) | GET | Retrieves all organization structures from NextLead. |

### Team Member

| Action | Method | Description |
| --- | --- | --- |
| [List Team Members](actions/list-team-members.md) | GET | Retrieves your organization's team members from NextLead. |

