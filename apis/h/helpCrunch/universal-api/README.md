# <img src="https://images.mindcloud.co/apps/icons/images-6_1774381394730.jpeg" alt="HelpCrunch logo" width="28" height="28"> HelpCrunch: Universal API

Manage customers, chats, messages, departments, and support activity in HelpCrunch.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/helpCrunch/latest
- **Category:** Support / Ticketing
- **Actions:** 29
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://helpcrunch.com
- **Vendor API docs:** https://docs.helpcrunch.com/en/rest-api-v1

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Customers](actions/list-customers.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/helpCrunch/latest/actions/list-customers?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (29)

### Application

| Action | Method | Description |
| --- | --- | --- |
| [List Applications](actions/list-applications.md) | GET | Retrieves a list of applications from HelpCrunch. |

### Chat

| Action | Method | Description |
| --- | --- | --- |
| [Create Chat](actions/create-chat.md) | POST | Creates a new chat in HelpCrunch. |
| [Get Chat](actions/get-chat.md) | GET | Retrieves a single chat from HelpCrunch. |
| [List Chats](actions/list-chats.md) | GET | Retrieves a list of chats from HelpCrunch. |
| [Mark Chat As Read By Agent](actions/mark-chat-as-read-by-agent.md) | PUT | Marks a chat as read by an agent in HelpCrunch. |
| [Mark Chat As Read By Customer](actions/mark-chat-as-read-by-customer.md) | PUT | Marks a chat as read by a customer in HelpCrunch. |
| [Rate Chat](actions/rate-chat.md) | PUT | Updates a chat's rating in HelpCrunch. |
| [Search Chats](actions/search-chats.md) | GET | Finds chats in HelpCrunch using search filters. |
| [Snooze Chat](actions/snooze-chat.md) | PUT | Updates a chat's snooze status in HelpCrunch. |
| [Update Chat Assignee](actions/update-chat-assignee.md) | PUT | Updates a chat's assignee in HelpCrunch. |
| [Update Chat Department](actions/update-chat-department.md) | PUT | Updates a chat's department in HelpCrunch. |
| [Update Chat Status](actions/update-chat-status.md) | PUT | Updates a chat's status in HelpCrunch. |

### Customer

| Action | Method | Description |
| --- | --- | --- |
| [Batch Update Customers](actions/batch-update-customers.md) | PUT | Updates multiple customer records in HelpCrunch. |
| [Create Customer](actions/create-customer.md) | POST | Creates a new customer in HelpCrunch. |
| [Delete Customer](actions/delete-customer.md) | DELETE | Deletes an existing customer from HelpCrunch. |
| [Get Customer](actions/get-customer.md) | GET | Retrieves a single customer from HelpCrunch. |
| [List Customers](actions/list-customers.md) | GET | Retrieves a list of customers from HelpCrunch. |
| [Search Customers](actions/search-customers.md) | GET | Finds customers in HelpCrunch using search filters. |
| [Tag Customer](actions/tag-customer.md) | PUT | Adds tags to a customer in HelpCrunch. |
| [Untag Customer](actions/untag-customer.md) | PUT | Removes tags from a customer in HelpCrunch. |
| [Update Customer](actions/update-customer.md) | PUT | Updates an existing customer in HelpCrunch. |

### Customer Event

| Action | Method | Description |
| --- | --- | --- |
| [Add Customer Event](actions/add-customer-event.md) | POST | Creates a new customer event in HelpCrunch. |

### Department

| Action | Method | Description |
| --- | --- | --- |
| [List Departments](actions/list-departments.md) | GET | Retrieves a list of departments from HelpCrunch. |

### Message

| Action | Method | Description |
| --- | --- | --- |
| [Create Agent Message](actions/create-agent-message.md) | POST | Creates an agent message in HelpCrunch. |
| [Create Customer Message](actions/create-customer-message.md) | POST | Creates a customer message in HelpCrunch. |
| [List Chat Messages](actions/list-chat-messages.md) | GET | Retrieves messages from a chat in HelpCrunch. |

### Organization

| Action | Method | Description |
| --- | --- | --- |
| [Get Team Availability Status](actions/get-team-availability-status.md) | GET | Retrieves team availability status from HelpCrunch. |

### Team Member

| Action | Method | Description |
| --- | --- | --- |
| [List Team Members](actions/list-team-members.md) | GET | Retrieves a list of team members from HelpCrunch. |
| [Unsubscribe Team Member](actions/unsubscribe-team-member.md) | PUT | Unsubscribes a team member in HelpCrunch. |

