# Autotask: Native API Reference

A consolidated summary of Autotask's API configuration and 35 documented operations, with links to official documentation.

- **Official docs:** https://www.autotask.net/help/developerhelp/Content/APIs/REST/REST_API_Home.htm
- **API base URL:** `https://webservices14.autotask.net/ATServicesRest/v1.0`

## Authentication

### Autotask API Credentials

Authenticate with an Autotask API-only username, secret, and integration code.

### Credentials

- **Username:** `username` · required · Autotask API-only user email.
- **Secret:** `password` · required · Secret for the Autotask API-only user.
- **API Integration Code:** `integrationCode` · required · Tracking identifier assigned to this integration.

Send these headers with each API request:

```http
Secret: <password>
Username: <username>
ApiIntegrationCode: <integrationCode>
```

[Official authentication documentation](https://www.autotask.net/help/DeveloperHelp/Content/APIs/REST/General_Topics/REST_Security_Auth.htm)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (35 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Count Contacts](actions/count-contacts.md) | `GET /Contacts/query/count` | [docs](https://www.autotask.net/help/developerhelp/Content/APIs/REST/Entities/ContactsEntity.htm) |
| [Count Opportunities](actions/count-opportunities.md) | `GET /Opportunities/query/count` | [docs](https://autotask.net/help/developerhelp/content/apis/rest/entities/OpportunitiesEntity.htm) |
| [Count Projects](actions/count-projects.md) | `GET /Projects/query/count` | [docs](https://autotask.net/help/developerhelp/content/APIs/REST/Entities/ProjectsEntity.htm) |
| [Create Contact](actions/create-contact.md) | `POST /Companies/:parentId/Contacts` | [docs](https://www.autotask.net/help/developerhelp/Content/APIs/REST/Entities/ContactsEntity.htm) |
| [Create Opportunity](actions/create-opportunity.md) | `POST /Opportunities` | [docs](https://www.autotask.net/help/developerhelp/Content/APIs/REST/Entities/OpportunitiesEntity.htm) |
| [Create Opportunity Attachment](actions/create-opportunity-attachment.md) | `POST /Opportunities/{opportunityId}/Attachments` | [docs](https://www.autotask.net/help/DeveloperHelp/Content/APIs/REST/API_Calls/REST_Attachments.htm) |
| [Create Project](actions/create-project.md) | `POST /Projects` | [docs](https://www.autotask.net/help/developerhelp/Content/APIs/REST/Entities/ProjectsEntity.htm) |
| [Delete Contact](actions/delete-contact.md) | `DELETE /Contacts/:id` | [docs](https://www.autotask.net/help/developerhelp/Content/APIs/REST/Entities/ContactsEntity.htm) |
| [Get Company](actions/get-company.md) | `GET /Companies/{id}` | [docs](https://autotask.net/help/developerhelp/content/APIs/REST/Entities/CompaniesEntity.htm) |
| [Get Contact](actions/get-contact.md) | `GET /Contacts/:id` | [docs](https://autotask.net/help/DeveloperHelp/Content/APIs/REST/Entities/ContactsEntity.htm) |
| [Get Contact Entity Information](actions/get-contact-entity-information.md) | `GET /Contacts/entityInformation` | [docs](https://www.autotask.net/help/developerhelp/Content/APIs/REST/Entities/ContactsEntity.htm) |
| [Get Contact Fields](actions/get-contact-fields.md) | `GET /Contacts/entityInformation/fields` | [docs](https://www.autotask.net/help/developerhelp/Content/APIs/REST/Entities/ContactsEntity.htm) |
| [Get Contact User-Defined Fields](actions/get-contact-user-defined-fields.md) | `GET /Contacts/entityInformation/userDefinedFields` | [docs](https://www.autotask.net/help/developerhelp/Content/APIs/REST/Entities/ContactsEntity.htm) |
| [Get Opportunity](actions/get-opportunity.md) | `GET /Opportunities/{id}` | [docs](https://autotask.net/help/developerhelp/content/apis/rest/entities/OpportunitiesEntity.htm) |
| [Get Opportunity Attachment](actions/get-opportunity-attachment.md) | `GET /OpportunityAttachments/{id}` | [docs](https://autotask.net/help/developerhelp/Content/APIs/REST/Entities/OpportunityAttachmentsEntity.htm) |
| [Get Opportunity Category](actions/get-opportunity-category.md) | `GET /OpportunityCategories/{id}` | [docs](https://autotask.net/help/developerhelp/content/apis/rest/Entities/OpportunityCategories.htm) |
| [Get Opportunity Fields](actions/get-opportunity-fields.md) | `GET /Opportunities/entityInformation/fields` | [docs](https://www.autotask.net/help/Developerhelp/Content/APIs/REST/API_Calls/REST_EntityInformationCall.htm) |
| [Get Opportunity User-Defined Fields](actions/get-opportunity-user-defined-fields.md) | `GET /Opportunities/entityInformation/userDefinedFields` | [docs](https://autotask.net/help/developerhelp/content/apis/rest/entities/OpportunitiesEntity.htm) |
| [Get Project](actions/get-project.md) | `GET /Projects/:id` | [docs](https://autotask.net/help/developerhelp/content/APIs/REST/Entities/ProjectsEntity.htm) |
| [Get Project Attachment](actions/get-project-attachment.md) | `GET /ProjectAttachments/{id}` | [docs](https://www.autotask.net/help/DeveloperHelp/Content/APIs/REST/Entities/ProjectAttachmentsEntity.htm) |
| [Get Project Entity Information](actions/get-project-entity-information.md) | `GET /Projects/entityInformation` | [docs](https://www.autotask.net/help/developerhelp/Content/APIs/REST/Entities/ProjectsEntity.htm) |
| [Get Project Fields](actions/get-project-fields.md) | `GET /Projects/entityInformation/fields` | [docs](https://www.autotask.net/help/Developerhelp/Content/APIs/REST/API_Calls/REST_EntityInformationCall.htm) |
| [Get Project User-Defined Fields](actions/get-project-user-defined-fields.md) | `GET /Projects/entityInformation/userDefinedFields` | [docs](https://autotask.net/help/developerhelp/content/APIs/REST/Entities/ProjectsEntity.htm) |
| [List Companies](actions/list-companies.md) | `GET /Companies/query` | [docs](https://autotask.net/help/developerhelp/content/APIs/REST/Entities/CompaniesEntity.htm) |
| [List Contacts](actions/list-contacts.md) | `GET /Contacts/query` | [docs](https://autotask.net/help/DeveloperHelp/Content/APIs/REST/Entities/ContactsEntity.htm) |
| [List Opportunities](actions/list-opportunities.md) | `GET /Opportunities/query` | [docs](https://autotask.net/help/developerhelp/content/apis/rest/entities/OpportunitiesEntity.htm) |
| [List Opportunity Attachments](actions/list-opportunity-attachments.md) | `GET /OpportunityAttachments/query` | [docs](https://autotask.net/help/developerhelp/Content/APIs/REST/Entities/OpportunityAttachmentsEntity.htm) |
| [List Opportunity Categories](actions/list-opportunity-categories.md) | `GET /OpportunityCategories/query` | [docs](https://autotask.net/help/developerhelp/content/apis/rest/Entities/OpportunityCategories.htm) |
| [List Project Attachments](actions/list-project-attachments.md) | `GET /ProjectAttachments/query` | [docs](https://www.autotask.net/help/DeveloperHelp/Content/APIs/REST/Entities/ProjectAttachmentsEntity.htm) |
| [List Projects](actions/list-projects.md) | `GET /Projects/query` | [docs](https://autotask.net/help/developerhelp/content/APIs/REST/Entities/ProjectsEntity.htm) |
| [List Resources](actions/list-resources.md) | `GET /Resources/query` | [docs](https://autotask.net/help/developerhelp/content/apis/rest/entities/ResourcesEntity.htm) |
| [Test Connection](actions/test-connection.md) | `GET /Version` | [docs](https://autotask.net/help/developerhelp/Content/APIs/REST/Entities/VersionEntity.htm) |
| [Update Contact](actions/update-contact.md) | `PATCH /Contacts` | [docs](https://www.autotask.net/help/developerhelp/Content/APIs/REST/Entities/ContactsEntity.htm) |
| [Update Opportunity](actions/update-opportunity.md) | `PATCH /Opportunities` | [docs](https://autotask.net/help/developerhelp/content/apis/rest/entities/OpportunitiesEntity.htm) |
| [Update Project](actions/update-project.md) | `PATCH /Projects` | [docs](https://www.autotask.net/help/developerhelp/Content/APIs/REST/Entities/ProjectsEntity.htm) |
