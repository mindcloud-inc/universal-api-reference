# <img src="https://images.mindcloud.co/apps/icons/id-ko3fn-nul-logos_1774979647081.jpeg" alt="Timelink logo" width="28" height="28"> Timelink: Universal API

Time tracking software for managing time entries, clients, projects, services, and users across Timelink's desktop, mobile, and web experiences.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/timelink/latest
- **Category:** Human Resources / HRIS
- **Actions:** 39
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://timelink.io
- **Vendor API docs:** https://api.timelink.io/documentation

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Company](actions/get-company.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/timelink/latest/actions/get-company?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (39)

### Client

| Action | Method | Description |
| --- | --- | --- |
| [Create Client](actions/create-client.md) | POST | Creates a client in the Timelink workspace. |
| [Delete Client](actions/delete-client.md) | DELETE | Deletes an existing client from Timelink. |
| [Get Client](actions/get-client.md) | GET | Retrieves a client from the Timelink workspace. |
| [List Clients](actions/list-clients.md) | GET | Retrieves clients from the Timelink workspace. |
| [Search Clients](actions/search-clients.md) | GET | Finds clients in the Timelink workspace. |
| [Update Client](actions/update-client.md) | PUT | Updates an existing client in Timelink. |

### Company

| Action | Method | Description |
| --- | --- | --- |
| [Get Company](actions/get-company.md) | GET | Retrieves company details from the Timelink workspace. |
| [Update Company Settings](actions/update-company-settings.md) | PUT | Updates company settings in the Timelink workspace. |

### Other

| Action | Method | Description |
| --- | --- | --- |
| [Delete Client by External ID](actions/delete-client-by-external-id.md) | DELETE | Deletes an existing client from Timelink by external ID. |
| [Update Client by External ID](actions/update-client-by-external-id.md) | PUT | Updates an existing client in Timelink by external ID. |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [Create Project](actions/create-project.md) | POST | Creates a project in the Timelink workspace. |
| [Delete Project](actions/delete-project.md) | DELETE | Deletes an existing project from Timelink. |
| [Get Project](actions/get-project.md) | GET | Retrieves a project from the Timelink workspace. |
| [List Projects](actions/list-projects.md) | GET | Retrieves projects from the Timelink workspace. |
| [Search Projects](actions/search-projects.md) | GET | Finds projects in the Timelink workspace. |
| [Update Project](actions/update-project.md) | PUT | Updates an existing project in Timelink. |
| [Update Project by External ID](actions/update-project-by-external-id.md) | PUT | Updates an existing project in Timelink by external ID. |

### Service

| Action | Method | Description |
| --- | --- | --- |
| [Create Service](actions/create-service.md) | POST | Creates a service in the Timelink workspace. |
| [Delete Service](actions/delete-service.md) | DELETE | Deletes an existing service from Timelink. |
| [Get Service](actions/get-service.md) | GET | Retrieves a service from the Timelink workspace. |
| [List Services](actions/list-services.md) | GET | Retrieves services from the Timelink workspace. |
| [Search Services](actions/search-services.md) | GET | Finds services in the Timelink workspace. |
| [Update Service](actions/update-service.md) | PUT | Updates an existing service in Timelink. |

### Time Entry

| Action | Method | Description |
| --- | --- | --- |
| [Create Time Entry](actions/create-time-entry.md) | POST | Creates a time entry in Timelink. |
| [Delete Time Entry](actions/delete-time-entry.md) | DELETE | Deletes an existing time entry from Timelink. |
| [Delete Time Entry by External ID](actions/delete-time-entry-by-external-id.md) | DELETE | Deletes an existing time entry from Timelink by external ID. |
| [Export Time Entries](actions/export-time-entries.md) | GET | Exports time entries from the Timelink workspace. |
| [Get Required Time Entry Fields](actions/get-required-time-entry-fields.md) | GET | Retrieves required time entry fields from Timelink. |
| [Get Time Entry](actions/get-time-entry.md) | GET | Retrieves a time entry from Timelink. |
| [Get Time Entry by External ID](actions/get-time-entry-by-external-id.md) | GET | Finds a time entry in Timelink by external ID. |
| [List Active Time Entries](actions/list-active-time-entries.md) | GET | Retrieves active time entries from Timelink. |
| [List Time Entries](actions/list-time-entries.md) | GET | Retrieves time entries from the Timelink workspace. |
| [List Time Entry Conflicts](actions/list-time-entry-conflicts.md) | GET | Retrieves time entry conflicts from Timelink. |
| [Search Time Entries](actions/search-time-entries.md) | GET | Finds time entries in the Timelink workspace. |
| [Update Time Entry](actions/update-time-entry.md) | PUT | Updates an existing time entry in Timelink. |
| [Update Time Entry by External ID](actions/update-time-entry-by-external-id.md) | PUT | Updates an existing time entry in Timelink by external ID. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Create User](actions/create-user.md) | POST | Creates a user in the Timelink workspace. |
| [Get User](actions/get-user.md) | GET | Retrieves a user from the Timelink workspace. |
| [List Users](actions/list-users.md) | GET | Retrieves users from the Timelink workspace. |

