# Beebole: Native API Reference

A consolidated summary of Beebole's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://beebole.com/help/api/
- **API base URL:** `https://beebole-apps.com/api/v2`

## Authentication

### API Token (Basic Auth)

Enter your Beebole API token in Username. Password must be x.

### Credentials

- **Username:** `username` · required
- **Password:** `password` · required

Join the username and password with a colon, Base64-encode the result, and send it with the `Basic` authorization scheme:

```js
const credentials = Buffer.from(`${username}:${password}`).toString('base64');

const response = await fetch(url, {
  headers: {
    Authorization: `Basic ${credentials}`
  }
});
```

[Official authentication documentation](https://beebole.com/help/api)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Activate a Company](actions/activate-a-company.md) | `POST` | [docs](https://beebole.com/help/api#activate-a-company) |
| [Activate a Person](actions/activate-a-person.md) | `POST` | [docs](https://beebole.com/help/api#activate-a-person) |
| [Activate a Project](actions/activate-a-project.md) | `POST` | [docs](https://beebole.com/help/api#activate-a-project) |
| [Activate a Subproject](actions/activate-a-subproject.md) | `POST` | [docs](https://beebole.com/help/api#activate-a-subproject) |
| [Activate a Task](actions/activate-a-task.md) | `POST` | [docs](https://beebole.com/help/api#activate-a-task) |
| [Approve Time Entry](actions/approve-time-entry.md) | `POST` | [docs](https://beebole.com/help/api#approve-time-entry) |
| [Create a Company](actions/create-a-company.md) | `POST` | [docs](https://beebole.com/help/api#create-a-company) |
| [Create a Person](actions/create-a-person.md) | `POST` | [docs](https://beebole.com/help/api#create-a-person) |
| [Create a Project](actions/create-a-project.md) | `POST` | [docs](https://beebole.com/help/api#create-a-project) |
| [Create a Subproject](actions/create-a-subproject.md) | `POST` | [docs](https://beebole.com/help/api#create-a-subproject) |
| [Create a Task](actions/create-a-task.md) | `POST` | [docs](https://beebole.com/help/api#create-a-task) |
| [Create a Time Entry](actions/create-a-time-entry.md) | `POST` | [docs](https://beebole.com/help/api#create-a-time-entry) |
| [Deactivate a Company](actions/deactivate-a-company.md) | `POST` | [docs](https://beebole.com/help/api#deactivate-a-company) |
| [Deactivate a Person](actions/deactivate-a-person.md) | `POST` | [docs](https://beebole.com/help/api#deactivate-a-person) |
| [Deactivate a Project](actions/deactivate-a-project.md) | `POST` | [docs](https://beebole.com/help/api#deactivate-a-project) |
| [Deactivate a Subproject](actions/deactivate-a-subproject.md) | `POST` | [docs](https://beebole.com/help/api#deactivate-a-subproject) |
| [Deactivate a Task](actions/deactivate-a-task.md) | `POST` | [docs](https://beebole.com/help/api#deactivate-a-task) |
| [Delete a Time Entry](actions/delete-a-time-entry.md) | `POST` | [docs](https://beebole.com/help/api#delete-a-time-entry) |
| [Get a Company](actions/get-a-company.md) | `POST` | [docs](https://beebole.com/help/api#get-a-company) |
| [Get a Person](actions/get-a-person.md) | `POST` | [docs](https://beebole.com/help/api#get-a-person) |
| [Get a Project](actions/get-a-project.md) | `POST` | [docs](https://beebole.com/help/api#get-a-project) |
| [Get a Subproject](actions/get-a-subproject.md) | `POST` | [docs](https://beebole.com/help/api#get-a-subproject) |
| [Get a Task](actions/get-a-task.md) | `POST` | [docs](https://beebole.com/help/api#get-a-task) |
| [Get a Time Entry](actions/get-a-time-entry.md) | `POST` | [docs](https://beebole.com/help/api#get-a-time-entry) |
| [Get Tasks to Create a Time Entry](actions/get-tasks-to-create-a-time-entry.md) | `POST` | [docs](https://beebole.com/help/api#get-tasks-to-create-a-time-entry) |
| [Get Time Entry Entities](actions/get-time-entry-entities.md) | `POST` | [docs](https://beebole.com/help/api#examples-) |
| [List Companies](actions/list-companies.md) | `POST` | [docs](https://beebole.com/help/api) |
| [List Persons](actions/list-persons.md) | `POST` | [docs](https://beebole.com/help/api#list-persons) |
| [List Projects](actions/list-projects.md) | `POST` | [docs](https://beebole.com/help/api#list-projects) |
| [List Subprojects](actions/list-subprojects.md) | `POST` | [docs](https://beebole.com/help/api#list-subprojects) |
| [List Tasks](actions/list-tasks.md) | `POST` | [docs](https://beebole.com/help/api#list-tasks) |
| [List Time Entries](actions/list-time-entries.md) | `POST` | [docs](https://beebole.com/help/api#list-time-entries) |
| [Reject Time Entry](actions/reject-time-entry.md) | `POST` | [docs](https://beebole.com/help/api#reject-time-entry) |
| [Submit Time Entry](actions/submit-time-entry.md) | `POST` | [docs](https://beebole.com/help/api#submit-time-entry) |
| [Update a Company](actions/update-a-company.md) | `POST` | [docs](https://beebole.com/help/api#update-a-company) |
| [Update a Person](actions/update-a-person.md) | `POST` | [docs](https://beebole.com/help/api#update-a-person) |
| [Update a Project](actions/update-a-project.md) | `POST` | [docs](https://beebole.com/help/api#update-a-project) |
| [Update a Subproject](actions/update-a-subproject.md) | `POST` | [docs](https://beebole.com/help/api#update-a-subproject) |
| [Update a Task](actions/update-a-task.md) | `POST` | [docs](https://beebole.com/help/api#update-a-task) |
| [Update a Time Entry](actions/update-a-time-entry.md) | `POST` | [docs](https://beebole.com/help/api#update-a-time-entry) |
