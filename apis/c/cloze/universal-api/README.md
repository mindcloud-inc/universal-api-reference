# <img src="https://images.mindcloud.co/apps/icons/cloze_1773855475809.png" alt="Cloze logo" width="28" height="28"> Cloze: Universal API

Manage relationships, projects, content, and analytics in Cloze

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/cloze/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://ai.cloze.com/
- **Vendor API docs:** https://developer.cloze.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get User Profile](actions/get-user-profile.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cloze/latest/actions/get-user-profile?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Communication Record

| Action | Method | Description |
| --- | --- | --- |
| [Add Communication Record](actions/add-communication-record.md) | POST | Creates a communication record in Cloze. |

### Company

| Action | Method | Description |
| --- | --- | --- |
| [Create Company](actions/create-company.md) | POST | Creates a company in Cloze. |
| [Delete Company](actions/delete-company.md) | DELETE | Deletes a company from Cloze. |
| [Get Company](actions/get-company.md) | GET | Retrieves a company from Cloze. |
| [Search Companies](actions/search-companies.md) | GET | Finds companies in Cloze. |
| [Stream Companies Feed](actions/stream-companies-feed.md) | GET | Retrieves the companies feed from Cloze. |
| [Update Company](actions/update-company.md) | PUT | Updates a company in Cloze. |

### Contact Segment

| Action | Method | Description |
| --- | --- | --- |
| [List Contact Segments](actions/list-contact-segments.md) | GET | Retrieves contact segments from Cloze. |

### Contact Stage

| Action | Method | Description |
| --- | --- | --- |
| [List People And Company Contact Stages](actions/list-people-and-company-contact-stages.md) | GET | Retrieves contact stages from Cloze. |

### Content Record

| Action | Method | Description |
| --- | --- | --- |
| [Add Content Record](actions/add-content-record.md) | POST | Creates a content record in Cloze. |

### Custom Field

| Action | Method | Description |
| --- | --- | --- |
| [List Custom Fields](actions/list-custom-fields.md) | GET | Retrieves custom fields from Cloze. |

### Email Open

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve Email Opens](actions/retrieve-email-opens.md) | GET | Retrieves email opens from Cloze. |

### Person

| Action | Method | Description |
| --- | --- | --- |
| [Create Person](actions/create-person.md) | POST | Creates a person in Cloze. |
| [Delete Person](actions/delete-person.md) | DELETE | Deletes a person from Cloze. |
| [Get Person](actions/get-person.md) | GET | Retrieves a person from Cloze. |
| [Search People](actions/search-people.md) | GET | Finds people in Cloze. |
| [Stream People Feed](actions/stream-people-feed.md) | GET | Retrieves the people feed from Cloze. |
| [Update Person](actions/update-person.md) | PUT | Updates a person in Cloze. |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [Create Project](actions/create-project.md) | POST | Creates a project in Cloze. |
| [Delete Project](actions/delete-project.md) | DELETE | Deletes a project from Cloze. |
| [Get Project](actions/get-project.md) | GET | Retrieves a project from Cloze. |
| [Search Projects](actions/search-projects.md) | GET | Finds projects in Cloze. |
| [Stream Projects Feed](actions/stream-projects-feed.md) | GET | Retrieves the projects feed from Cloze. |
| [Update Project](actions/update-project.md) | PUT | Updates a project in Cloze. |

### Project Segment

| Action | Method | Description |
| --- | --- | --- |
| [List Project Segments](actions/list-project-segments.md) | GET | Retrieves project segments from Cloze. |

### Project Stage

| Action | Method | Description |
| --- | --- | --- |
| [List Project Stages](actions/list-project-stages.md) | GET | Retrieves project stages from Cloze. |

### Step

| Action | Method | Description |
| --- | --- | --- |
| [List Steps](actions/list-steps.md) | GET | Retrieves steps from Cloze. |

### To Do

| Action | Method | Description |
| --- | --- | --- |
| [Create To Do](actions/create-to-do.md) | POST | Creates a to-do in Cloze. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get User Profile](actions/get-user-profile.md) | GET | Retrieves a user profile from Cloze. |

### View Audience

| Action | Method | Description |
| --- | --- | --- |
| [List Views And Audiences](actions/list-views-and-audiences.md) | GET | Retrieves views and audiences from Cloze. |

