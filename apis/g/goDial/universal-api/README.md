# <img src="https://images.mindcloud.co/apps/icons/captura-de-tela-2026-04-23-as-11_1776954178951.png" alt="GoDial logo" width="28" height="28"> GoDial: Universal API

SIM-based autodialer and CRM for managing teams, accounts, lists, contacts, tasks, and call logs.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/goDial/latest
- **Category:** Support / Contact Center
- **Actions:** 31
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://godial.cc
- **Vendor API docs:** https://godial.stoplight.io/docs/godial/cd4edf0828dd6-go-dial-crm-external-api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Teams](actions/team-list.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/goDial/latest/actions/team-list?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (31)

### Calls

| Action | Method | Description |
| --- | --- | --- |
| [List Call Logs](actions/log-list.md) | GET | Retrieves a list of call logs from GoDial. |

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact](actions/contact-add.md) | POST | Creates a new contact in GoDial. |
| [Move Contact to List](actions/contact-change-list.md) | PUT | Moves a contact to another list in GoDial. |
| [Delete Contact by Phone Number](actions/contact-delete-by-phone-number.md) | DELETE | Deletes a contact from GoDial by phone number and list ID. |
| [Log Contact Disposition](actions/contact-dispose.md) | PUT | Logs a disposition for a contact in GoDial. |
| [List Contacts](actions/contact-list.md) | GET | Retrieves contacts from a specific GoDial contact list. |
| [Delete Contact](actions/contact-remove.md) | DELETE | Deletes an existing contact from GoDial. |
| [Update Contact](actions/contact-update.md) | PUT | Updates an existing contact in GoDial. |
| [Get Contact](actions/contact-view.md) | GET | Retrieves details for a contact from GoDial. |

### Lists

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact List](actions/lists-add.md) | POST | Creates a new contact list in GoDial. |
| [Assign Contact List to User](actions/lists-assign.md) | PUT | Assigns a contact list to a user in GoDial. |
| [Unassign Contact List from User](actions/lists-detach.md) | PUT | Unassigns a contact list from a user in GoDial. |
| [List Contact Lists](actions/lists-list.md) | GET | Retrieves a list of contact lists from GoDial. |
| [Delete Contact List](actions/lists-remove.md) | DELETE | Deletes an existing contact list from GoDial. |
| [Update Contact List](actions/lists-update.md) | PUT | Updates an existing contact list in GoDial. |
| [Get Contact List](actions/lists-view.md) | GET | Retrieves a contact list from GoDial. |

### Tasks

| Action | Method | Description |
| --- | --- | --- |
| [Create Task](actions/task-add.md) | POST | Creates a new task in GoDial. |
| [List Tasks](actions/task-list.md) | GET | Retrieves a list of tasks from GoDial. |
| [Delete Task](actions/task-remove.md) | DELETE | Deletes an existing task from GoDial. |
| [Update Task](actions/task-update.md) | PUT | Updates an existing task in GoDial. |
| [Get Task](actions/task-view.md) | GET | Retrieves details for a task from GoDial. |

### Teams

| Action | Method | Description |
| --- | --- | --- |
| [Create Team](actions/team-add.md) | POST | Creates a new team in GoDial. |
| [List Teams](actions/team-list.md) | GET | Retrieves a list of teams from GoDial. |
| [Delete Team](actions/team-remove.md) | DELETE | Deletes an existing team from GoDial. |
| [Update Team](actions/team-update.md) | PUT | Updates an existing team in GoDial. |
| [Get Team](actions/team-view.md) | GET | Retrieves details for a team from GoDial. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Create User](actions/accounts-add.md) | POST | Creates a new user in GoDial. |
| [List Users](actions/accounts-list.md) | GET | Retrieves a list of users from GoDial. |
| [Delete User](actions/accounts-remove.md) | DELETE | Deletes an existing user from GoDial. |
| [Update User](actions/accounts-update.md) | PUT | Updates an existing user in GoDial. |
| [Get User](actions/accounts-view.md) | GET | Retrieves details for a user from GoDial. |

