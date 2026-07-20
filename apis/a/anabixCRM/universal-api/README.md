# <img src="https://images.mindcloud.co/apps/icons/anabix-crm-icon-unplated_1775860706604.png" alt="Anabix CRM logo" width="28" height="28"> Anabix CRM: Universal API

Manage Anabix CRM contacts, companies, deals, tasks, activities, lists, and users.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/anabixCRM/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 25
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.anabix.cz
- **Vendor API docs:** https://www.anabix.cz/wp-content/uploads/2025/02/anabix_api_manual-2025.pdf

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Contacts](actions/list-contacts.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/anabixCRM/latest/actions/list-contacts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (25)

### Activity

| Action | Method | Description |
| --- | --- | --- |
| [Create Activity](actions/create-activity.md) | POST | Creates a new activity in Anabix CRM. |
| [Get Activity](actions/get-activity.md) | GET | Retrieves an activity from Anabix CRM. |
| [List Activities](actions/list-activities.md) | GET | Retrieves activity records from Anabix CRM. |
| [Update Activity](actions/update-activity.md) | PUT | Updates an existing activity in Anabix CRM. |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | POST | Creates a new contact in Anabix CRM. |
| [Get Contact](actions/get-contact.md) | GET | Retrieves a contact from Anabix CRM. |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves contact records from Anabix CRM. |
| [Manage Contact Lists](actions/manage-contact-lists.md) | PUT | Updates contact list memberships in Anabix CRM. |
| [Update Contact](actions/update-contact.md) | PUT | Updates an existing contact in Anabix CRM. |

### Deal

| Action | Method | Description |
| --- | --- | --- |
| [Create Deal](actions/create-deal.md) | POST | Creates a new deal in Anabix CRM. |
| [Get Deal](actions/get-deal.md) | GET | Retrieves a deal from Anabix CRM. |
| [List Deals](actions/list-deals.md) | GET | Retrieves deal records from Anabix CRM. |
| [Update Deal](actions/update-deal.md) | PUT | Updates an existing deal in Anabix CRM. |

### List

| Action | Method | Description |
| --- | --- | --- |
| [Create List](actions/create-list.md) | POST | Creates a new list in Anabix CRM. |
| [Get List](actions/get-list.md) | GET | Retrieves a list from Anabix CRM. |
| [List Lists](actions/list-lists.md) | GET | Retrieves list records from Anabix CRM. |

### Organization

| Action | Method | Description |
| --- | --- | --- |
| [Create Organization](actions/create-organization.md) | POST | Creates a new organization in Anabix CRM. |
| [Get Organization](actions/get-organization.md) | GET | Retrieves an organization from Anabix CRM. |
| [List Organizations](actions/list-organizations.md) | GET | Retrieves organization records from Anabix CRM. |
| [Update Organization](actions/update-organization.md) | PUT | Updates an existing organization in Anabix CRM. |

### Task

| Action | Method | Description |
| --- | --- | --- |
| [Create Task](actions/create-task.md) | POST | Creates a new task in Anabix CRM. |
| [Get Task](actions/get-task.md) | GET | Retrieves a task from Anabix CRM. |
| [List Tasks](actions/list-tasks.md) | GET | Retrieves task records from Anabix CRM. |
| [Update Task](actions/update-task.md) | PUT | Updates an existing task in Anabix CRM. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [List Active Users](actions/list-active-users.md) | GET | Retrieves active users from Anabix CRM. |

