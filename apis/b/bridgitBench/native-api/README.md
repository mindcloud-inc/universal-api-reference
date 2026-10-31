# Bridgit Bench: Native API Reference

A consolidated summary of Bridgit Bench's API configuration and 200 documented operations, with links to official documentation.

- **Official docs:** https://developers.gobridgit.com/reference
- **OpenAPI specification:** https://bench.gobridgit.com/rp/swagger/v1/swagger.json
- **API base URL:** `https://bench.gobridgit.com`

## Authentication

### Service Account

### Credentials

- **Service Account Password:** `password` · required
- **Service Account ID:** `username` · required

Send these headers with each API request:

```http
Authorization: Bearer <custom.accessToken>
```

[Official authentication documentation](https://developers.gobridgit.com/docs/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (default 25; minimum 1). Use `offset` in the query string as the record offset.

## Endpoints (200 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Clear Person Field Values](actions/clear-person-field-values.md) | `DELETE /rp/api/v1/accounts/:accountId/persons/:personId/person-field-values` | [docs](https://developers.gobridgit.com/reference/personfieldvalue_clearfieldvalues) |
| [Clear Project Field Values](actions/clear-project-field-values.md) | `DELETE /rp/api/v1/accounts/:accountId/projects/:projectId/project-field-values` | [docs](https://developers.gobridgit.com/reference/projectfieldvalue_clearfieldvalues) |
| [Create Account Certification](actions/create-account-certification.md) | `POST /rp/api/v1/accounts/:accountId/certifications` | [docs](https://developers.gobridgit.com/reference/accountcertifications_add) |
| [Create Account Grouping](actions/create-account-grouping.md) | `POST /rp/api/v1/accounts/:accountId/groupings` | [docs](https://developers.gobridgit.com/reference/accountgroupings_add) |
| [Create Account Phase](actions/create-account-phase.md) | `POST /rp/api/v1/accounts/:accountId/Phases` | [docs](https://developers.gobridgit.com/reference/phases_add) |
| [Create Experience Field Values](actions/create-experience-field-values.md) | `POST /rp/api/v1/accounts/:accountId/experience-fields/:experienceFieldId/values` | [docs](https://developers.gobridgit.com/reference/experiencefieldvalues_create) |
| [Create Hourly Allocation](actions/create-hourly-allocation.md) | `POST /rp/api/v1/accounts/:accountId/projects/:projectId/hourly-allocations` | [docs](https://developers.gobridgit.com/reference/hourlyallocations_post) |
| [Create Person](actions/create-person.md) | `POST /rp/api/v1/accounts/:accountId/Persons` | [docs](https://developers.gobridgit.com/reference/persons_post) |
| [Create Person Attachment](actions/create-person-attachment.md) | `POST /rp/api/v1/accounts/:accountId/persons/:personId/attachments` | [docs](https://developers.gobridgit.com/reference/personattachments_post) |
| [Create Person Certification](actions/create-person-certification.md) | `POST /rp/api/v1/accounts/:accountId/persons/:personId/certifications` | [docs](https://developers.gobridgit.com/reference/personcertifications_add) |
| [Create Person Employment Period](actions/create-person-employment-period.md) | `POST /rp/api/v1/accounts/:accountId/persons/:personId/employment-periods` | [docs](https://developers.gobridgit.com/reference/personemploymentperiods_add) |
| [Create Person Historical Experience](actions/create-person-historical-experience.md) | `POST /rp/api/v1/accounts/:accountId/persons/:personId/historical-experiences` | [docs](https://developers.gobridgit.com/reference/personhistoricalexperiences_post) |
| [Create Person Historical Experience Field](actions/create-person-historical-experience-field.md) | `POST /rp/api/v1/accounts/:accountId/persons/:personId/historical-experiences/:historicalExperienceId/experience-fields` | [docs](https://developers.gobridgit.com/reference/personhistoricalexperiencefields_post) |
| [Create Person Title](actions/create-person-title.md) | `POST /rp/api/v1/accounts/:accountId/persons/:personId/titles` | [docs](https://developers.gobridgit.com/reference/persontitles_add) |
| [Create Person Unavailabilities](actions/create-person-unavailabilities.md) | `POST /rp/api/v1/accounts/:accountId/persons/:id/unavailabilities` | [docs](https://developers.gobridgit.com/reference/personunavailabilities_addunavailabilities) |
| [Create Project](actions/create-project.md) | `POST /rp/api/v1/accounts/:accountId/Projects` | [docs](https://developers.gobridgit.com/reference/projects_post) |
| [Create Project Allocation](actions/create-project-allocation.md) | `POST /rp/api/v1/accounts/:accountId/projects/:projectId/Allocations` | [docs](https://developers.gobridgit.com/reference/allocations_post) |
| [Create Project Note](actions/create-project-note.md) | `POST /rp/api/v1/accounts/:accountId/projects/:projectId/notes` | [docs](https://developers.gobridgit.com/reference/projectnotes_add) |
| [Create Project Phase](actions/create-project-phase.md) | `POST /rp/api/v1/accounts/:accountId/projects/:projectId/phases` | [docs](https://developers.gobridgit.com/reference/projectsphases_add) |
| [Create Project Phases in Bulk](actions/create-project-phases-in-bulk.md) | `POST /rp/api/v1/accounts/:accountId/projects/:projectId/phases/bulk` | [docs](https://developers.gobridgit.com/reference/projectsphases_bulkadd) |
| [Create Project Role](actions/create-project-role.md) | `POST /rp/api/v1/accounts/:accountId/projects/:projectId/roles` | [docs](https://developers.gobridgit.com/reference/projectroles_add) |
| [Create Project Role Categories](actions/create-project-role-categories.md) | `POST /rp/api/v1/accounts/:accountId/projects/:projectId/role-categories` | [docs](https://developers.gobridgit.com/reference/projectrolecategories_add) |
| [Create Project Roles in Bulk](actions/create-project-roles-in-bulk.md) | `POST /rp/api/v1/accounts/:accountId/projects/:projectId/roles/bulk` | [docs](https://developers.gobridgit.com/reference/projectroles_bulkadd) |
| [Create Project Task Role](actions/create-project-task-role.md) | `POST /rp/api/v1/accounts/:accountId/projects/:projectId/tasks/:id/roles` | [docs](https://developers.gobridgit.com/reference/projecttasks_addrole) |
| [Create Project Task Role Allocation](actions/create-project-task-role-allocation.md) | `POST /rp/api/v1/accounts/:accountId/projects/:projectId/tasks/:taskId/roles/:id/allocations` | [docs](https://developers.gobridgit.com/reference/projecttasks_addallocation) |
| [Create Project Task Role Allocations in Bulk](actions/create-project-task-role-allocations-in-bulk.md) | `POST /rp/api/v1/accounts/:accountId/projects/:projectId/tasks/:taskId/roles/allocations/bulk` | [docs](https://developers.gobridgit.com/reference/projecttasks_bulkaddallocation) |
| [Create Project Task Roles in Bulk](actions/create-project-task-roles-in-bulk.md) | `POST /rp/api/v1/accounts/:accountId/projects/:projectId/tasks/:id/roles/bulk` | [docs](https://developers.gobridgit.com/reference/projecttasks_bulkaddroles) |
| [Create Project Tasks](actions/create-project-tasks.md) | `POST /rp/api/v1/accounts/:accountId/projects/:projectId/tasks` | [docs](https://developers.gobridgit.com/reference/projecttasks_add) |
| [Create Project Tasks from Templates](actions/create-project-tasks-from-templates.md) | `POST /rp/api/v1/accounts/:accountId/projects/:projectId/tasks/by-templates` | [docs](https://developers.gobridgit.com/reference/projecttasks_addtasksbytemplates) |
| [Create Role Allocation](actions/create-role-allocation.md) | `POST /rp/api/v1/accounts/:accountId/projects/:projectId/roles/:roleId/allocations` | [docs](https://developers.gobridgit.com/reference/roleallocations_post) |
| [Create Saved Filter](actions/create-saved-filter.md) | `POST /rp/api/v1/accounts/:accountId/my-filters` | [docs](https://developers.gobridgit.com/reference/userfilters_add) |
| [Create Service Account](actions/create-service-account.md) | `POST /rp/api/v1/accounts/:accountId/service-accounts` | [docs](https://developers.gobridgit.com/reference/serviceaccounts_createserviceaccount) |
| [Deactivate Account User](actions/deactivate-account-user.md) | `DELETE /rp/api/v1/accounts/:accountId/users/:id` | [docs](https://developers.gobridgit.com/reference/accountusers_delete) |
| [Deactivate Person](actions/deactivate-person.md) | `DELETE /rp/api/v1/accounts/:accountId/Persons/:id` | [docs](https://developers.gobridgit.com/reference/persons_delete) |
| [Deactivate Person with Details](actions/deactivate-person-with-details.md) | `POST /rp/api/v1/accounts/:accountId/Persons/:id/deactivate` | [docs](https://developers.gobridgit.com/reference/persons_deactivate) |
| [Deactivate Service Account](actions/deactivate-service-account.md) | `DELETE /rp/api/v1/accounts/:accountId/service-accounts/:id` | [docs](https://developers.gobridgit.com/reference/serviceaccounts_deactivateserviceaccount) |
| [Delete Account Certification](actions/delete-account-certification.md) | `DELETE /rp/api/v1/accounts/:accountId/certifications/:id` | [docs](https://developers.gobridgit.com/reference/accountcertifications_delete) |
| [Delete Account Grouping](actions/delete-account-grouping.md) | `DELETE /rp/api/v1/accounts/:accountId/groupings/:id` | [docs](https://developers.gobridgit.com/reference/accountgroupings_delete) |
| [Delete Account Invitation](actions/delete-account-invitation.md) | `DELETE /rp/api/v1/accounts/:accountId/invitations/:id` | [docs](https://developers.gobridgit.com/reference/accountinvitations_delete) |
| [Delete Account Phases](actions/delete-account-phases.md) | `DELETE /rp/api/v1/accounts/:accountId/Phases` | [docs](https://developers.gobridgit.com/reference/phases_delete) |
| [Delete Experience Field Value](actions/delete-experience-field-value.md) | `DELETE /rp/api/v1/accounts/:accountId/experience-fields/:experienceFieldId/values/:experienceFieldValueId` | [docs](https://developers.gobridgit.com/reference/experiencefieldvalues_delete) |
| [Delete Hourly Allocation](actions/delete-hourly-allocation.md) | `DELETE /rp/api/v1/accounts/:accountId/projects/:projectId/hourly-allocations` | [docs](https://developers.gobridgit.com/reference/hourlyallocations_delete) |
| [Delete Hourly Role Names](actions/delete-hourly-role-names.md) | `DELETE /rp/api/v1/accounts/:id/hourly-role-names` | [docs](https://developers.gobridgit.com/reference/hourlyrolenames_delete) |
| [Delete Person Attachment](actions/delete-person-attachment.md) | `DELETE /rp/api/v1/accounts/:accountId/persons/:personId/attachments/:id` | [docs](https://developers.gobridgit.com/reference/personattachments_delete) |
| [Delete Person Certification](actions/delete-person-certification.md) | `DELETE /rp/api/v1/accounts/:accountId/persons/:personId/certifications/:id` | [docs](https://developers.gobridgit.com/reference/personcertifications_delete) |
| [Delete Person Certification Attachment](actions/delete-person-certification-attachment.md) | `DELETE /rp/api/v1/accounts/:accountId/persons/:personId/certifications/:certId/attachments/:id` | [docs](https://developers.gobridgit.com/reference/personcertattachments_delete) |
| [Delete Person Employment Period](actions/delete-person-employment-period.md) | `DELETE /rp/api/v1/accounts/:accountId/persons/:personId/employment-periods/:periodId` | [docs](https://developers.gobridgit.com/reference/personemploymentperiods_remove) |
| [Delete Person Fields](actions/delete-person-fields.md) | `DELETE /rp/api/v1/accounts/:id/person-fields` | [docs](https://developers.gobridgit.com/reference/personfields_delete) |
| [Delete Person Grouping](actions/delete-person-grouping.md) | `DELETE /rp/api/v1/accounts/:accountId/persons/:personId/groupings/:id` | [docs](https://developers.gobridgit.com/reference/persongroupings_remove) |
| [Delete Person Historical Experience](actions/delete-person-historical-experience.md) | `DELETE /rp/api/v1/accounts/:accountId/persons/:personId/historical-experiences/:historicalExperienceId` | [docs](https://developers.gobridgit.com/reference/personhistoricalexperiences_delete) |
| [Delete Person Historical Experience Field](actions/delete-person-historical-experience-field.md) | `DELETE /rp/api/v1/accounts/:accountId/persons/:personId/historical-experiences/:historicalExperienceId/experience-fields/:experienceFieldId` | [docs](https://developers.gobridgit.com/reference/personhistoricalexperiencefields_delete) |
| [Delete Person Profile Picture](actions/delete-person-profile-picture.md) | `DELETE /rp/api/v1/accounts/:accountId/persons/:personId/profile-picture` | [docs](https://developers.gobridgit.com/reference/personprofile_delete) |
| [Delete Person Title](actions/delete-person-title.md) | `DELETE /rp/api/v1/accounts/:accountId/persons/:personId/titles/:entryId` | [docs](https://developers.gobridgit.com/reference/persontitles_remove) |
| [Delete Person Unavailabilities](actions/delete-person-unavailabilities.md) | `DELETE /rp/api/v1/accounts/:accountId/persons/:id/unavailabilities` | [docs](https://developers.gobridgit.com/reference/personunavailabilities_deleteunavailabilities) |
| [Delete Project](actions/delete-project.md) | `DELETE /rp/api/v1/accounts/:accountId/Projects/:id` | [docs](https://developers.gobridgit.com/reference/projects_delete) |
| [Delete Project Allocation](actions/delete-project-allocation.md) | `DELETE /rp/api/v1/accounts/:accountId/projects/:projectId/Allocations` | [docs](https://developers.gobridgit.com/reference/allocations_delete) |
| [Delete Project Fields](actions/delete-project-fields.md) | `DELETE /rp/api/v1/accounts/:id/project-fields` | [docs](https://developers.gobridgit.com/reference/projectfields_delete) |
| [Delete Project Grouping](actions/delete-project-grouping.md) | `DELETE /rp/api/v1/accounts/:accountId/projects/:projectId/groupings/:id` | [docs](https://developers.gobridgit.com/reference/projectgroupings_remove) |
| [Delete Project Note](actions/delete-project-note.md) | `DELETE /rp/api/v1/accounts/:accountId/projects/:projectId/notes/:id` | [docs](https://developers.gobridgit.com/reference/projectnotes_delete) |
| [Delete Project Phase](actions/delete-project-phase.md) | `DELETE /rp/api/v1/accounts/:accountId/projects/:projectId/phases/:phaseId` | [docs](https://developers.gobridgit.com/reference/projectsphases_delete) |
| [Delete Project Phases in Bulk](actions/delete-project-phases-in-bulk.md) | `DELETE /rp/api/v1/accounts/:accountId/projects/:projectId/phases` | [docs](https://developers.gobridgit.com/reference/projectsphases_bulkdelete) |
| [Delete Project Role](actions/delete-project-role.md) | `DELETE /rp/api/v1/accounts/:accountId/projects/:projectId/roles/:id` | [docs](https://developers.gobridgit.com/reference/projectroles_remove) |
| [Delete Project Role Categories](actions/delete-project-role-categories.md) | `DELETE /rp/api/v1/accounts/:accountId/projects/:projectId/role-categories` | [docs](https://developers.gobridgit.com/reference/projectrolecategories_remove) |
| [Delete Project Roles in Bulk](actions/delete-project-roles-in-bulk.md) | `DELETE /rp/api/v1/accounts/:accountId/projects/:projectId/roles/bulk` | [docs](https://developers.gobridgit.com/reference/projectroles_bulkremove) |
| [Delete Project Task](actions/delete-project-task.md) | `DELETE /rp/api/v1/accounts/:accountId/projects/:projectId/tasks/:id` | [docs](https://developers.gobridgit.com/reference/projecttasks_remove) |
| [Delete Project Task Role](actions/delete-project-task-role.md) | `DELETE /rp/api/v1/accounts/:accountId/projects/:projectId/tasks/:taskId/roles/:id` | [docs](https://developers.gobridgit.com/reference/projecttasks_removerole) |
| [Delete Role Names](actions/delete-role-names.md) | `DELETE /rp/api/v1/accounts/:accountId/role-names` | [docs](https://developers.gobridgit.com/reference/rolenames_delete) |
| [Delete Saved Filter](actions/delete-saved-filter.md) | `DELETE /rp/api/v1/accounts/:accountId/my-filters/:id` | [docs](https://developers.gobridgit.com/reference/userfilters_delete) |
| [Delete Shared Filter](actions/delete-shared-filter.md) | `DELETE /rp/api/v1/accounts/:accountId/shared-filters/:id` | [docs](https://developers.gobridgit.com/reference/sharedfilters_delete) |
| [Demote Experience Field](actions/demote-experience-field.md) | `DELETE /rp/api/v1/accounts/:accountId/experience-fields/:experienceFieldId` | [docs](https://developers.gobridgit.com/reference/experiencefields_demoteexperiencefield) |
| [Get Account](actions/get-account.md) | `GET /rp/api/v1/Accounts/:id` | [docs](https://developers.gobridgit.com/reference/accounts_get) |
| [Get Account Certification](actions/get-account-certification.md) | `GET /rp/api/v1/accounts/:accountId/certifications/:id` | [docs](https://developers.gobridgit.com/reference/accountcertifications_get) |
| [Get Account Grouping](actions/get-account-grouping.md) | `GET /rp/api/v1/accounts/:accountId/groupings/:id` | [docs](https://developers.gobridgit.com/reference/accountgroupings_get) |
| [Get Account Integration](actions/get-account-integration.md) | `GET /rp/api/v1/accounts/:accountId/integrations` | [docs](https://developers.gobridgit.com/reference/accountintegrations_get) |
| [Get Account Phase](actions/get-account-phase.md) | `GET /rp/api/v1/accounts/:accountId/Phases/:id` | [docs](https://developers.gobridgit.com/reference/phases_get) |
| [Get Account User](actions/get-account-user.md) | `GET /rp/api/v1/accounts/:accountId/users/:id` | [docs](https://developers.gobridgit.com/reference/accountusers_get) |
| [Get My Person Profile](actions/get-my-person-profile.md) | `GET /rp/api/v1/accounts/:accountId/persons/me` | [docs](https://developers.gobridgit.com/reference/personprofile_getmine) |
| [Get Person](actions/get-person.md) | `GET /rp/api/v1/accounts/:accountId/Persons/:id` | [docs](https://developers.gobridgit.com/reference/persons_get) |
| [Get Person Attachment](actions/get-person-attachment.md) | `GET /rp/api/v1/accounts/:accountId/persons/:personId/attachments/:id` | [docs](https://developers.gobridgit.com/reference/personattachments_get) |
| [Get Person by External ID](actions/get-person-by-external-id.md) | `GET /rp/api/v1/accounts/:accountId/external/persons/:externalId` | [docs](https://developers.gobridgit.com/reference/external_getperson) |
| [Get Person Certification](actions/get-person-certification.md) | `GET /rp/api/v1/accounts/:accountId/persons/:personId/certifications/:id` | [docs](https://developers.gobridgit.com/reference/personcertifications_get) |
| [Get Person Certification Attachment](actions/get-person-certification-attachment.md) | `GET /rp/api/v1/accounts/:accountId/persons/:personId/certifications/:certId/attachments/:id` | [docs](https://developers.gobridgit.com/reference/personcertattachments_get) |
| [Get Person Employment History](actions/get-person-employment-history.md) | `GET /rp/api/v1/accounts/:accountId/persons/:personId/employment-periods` | [docs](https://developers.gobridgit.com/reference/personemploymentperiods_get) |
| [Get Person Historical Experience](actions/get-person-historical-experience.md) | `GET /rp/api/v1/accounts/:accountId/persons/:personId/historical-experiences/:historicalExperienceId` | [docs](https://developers.gobridgit.com/reference/personhistoricalexperiences_getone) |
| [Get Person Title History](actions/get-person-title-history.md) | `GET /rp/api/v1/accounts/:accountId/persons/:personId/titles` | [docs](https://developers.gobridgit.com/reference/persontitles_get) |
| [Get Project](actions/get-project.md) | `GET /rp/api/v1/accounts/:accountId/Projects/:id` | [docs](https://developers.gobridgit.com/reference/projects_get) |
| [Get Project by External ID](actions/get-project-by-external-id.md) | `GET /rp/api/v1/accounts/:accountId/external/projects/:externalId` | [docs](https://developers.gobridgit.com/reference/external_getproject) |
| [Get Project Note](actions/get-project-note.md) | `GET /rp/api/v1/accounts/:accountId/projects/:projectId/notes/:id` | [docs](https://developers.gobridgit.com/reference/projectnotes_get) |
| [Get Project Role](actions/get-project-role.md) | `GET /rp/api/v1/accounts/:accountId/projects/:projectId/roles/:id` | [docs](https://developers.gobridgit.com/reference/projectroles_get) |
| [Get Project Role by External ID](actions/get-project-role-by-external-id.md) | `GET /rp/api/v1/accounts/:accountId/external/roles/:externalId` | [docs](https://developers.gobridgit.com/reference/external_getprojectrole) |
| [Get Saved Filter](actions/get-saved-filter.md) | `GET /rp/api/v1/accounts/:accountId/my-filters/:id` | [docs](https://developers.gobridgit.com/reference/userfilters_get) |
| [Get Workforce Spend Hours Breakdown](actions/get-workforce-spend-hours-breakdown.md) | `POST /rp/api/v1/accounts/:accountId/projects/:projectId/workforce-spend-reports/hours-breakdown` | [docs](https://developers.gobridgit.com/reference/projectworkforcespendreports_getworkforcespendreportsbreakdownhours) |
| [Get Workforce Spend Hours Overview](actions/get-workforce-spend-hours-overview.md) | `POST /rp/api/v1/accounts/:accountId/projects/:projectId/workforce-spend-reports/hours-overview` | [docs](https://developers.gobridgit.com/reference/projectworkforcespendreports_getworkforcespendreportsoverviewhours) |
| [Link Person Certification Attachment](actions/link-person-certification-attachment.md) | `POST /rp/api/v1/accounts/:accountId/persons/:personId/certifications/:certId/attachments` | [docs](https://developers.gobridgit.com/reference/personcertattachments_post) |
| [List Account Certifications](actions/list-account-certifications.md) | `GET /rp/api/v1/accounts/:accountId/certifications` | [docs](https://developers.gobridgit.com/reference/accountcertifications_query) |
| [List Account Groupings](actions/list-account-groupings.md) | `GET /rp/api/v1/accounts/:accountId/groupings` | [docs](https://developers.gobridgit.com/reference/accountgroupings_query) |
| [List Account Hourly Roles](actions/list-account-hourly-roles.md) | `GET /rp/api/v1/Accounts/:id/hourly-roles` | [docs](https://developers.gobridgit.com/reference/accounts_queryhourlyroles) |
| [List Account Invitations](actions/list-account-invitations.md) | `GET /rp/api/v1/accounts/:accountId/invitations` | [docs](https://developers.gobridgit.com/reference/accountinvitations_query) |
| [List Account Person Certifications](actions/list-account-person-certifications.md) | `GET /rp/api/v1/Accounts/:id/person-certifications` | [docs](https://developers.gobridgit.com/reference/accounts_querypersoncertifications) |
| [List Account Person Field Values](actions/list-account-person-field-values.md) | `GET /rp/api/v1/Accounts/:id/person-field-values` | [docs](https://developers.gobridgit.com/reference/accounts_queryprofiles) |
| [List Account Person Unavailabilities](actions/list-account-person-unavailabilities.md) | `GET /rp/api/v1/accounts/:accountId/persons/unavailabilities` | [docs](https://developers.gobridgit.com/reference/personunavailabilities_query) |
| [List Account Phases](actions/list-account-phases.md) | `GET /rp/api/v1/accounts/:accountId/Phases` | [docs](https://developers.gobridgit.com/reference/phases_query) |
| [List Account Project Field Values](actions/list-account-project-field-values.md) | `GET /rp/api/v1/Accounts/:id/project-field-values` | [docs](https://developers.gobridgit.com/reference/accounts_queryprojectfieldvalues) |
| [List Account Role Categories](actions/list-account-role-categories.md) | `GET /rp/api/v1/Accounts/:id/role-categories` | [docs](https://developers.gobridgit.com/reference/accounts_queryrolecategories) |
| [List Account Salaried Roles](actions/list-account-salaried-roles.md) | `GET /rp/api/v1/Accounts/:id/roles` | [docs](https://developers.gobridgit.com/reference/accounts_queryroles) |
| [List Account Tasks](actions/list-account-tasks.md) | `GET /rp/api/v1/Accounts/:id/tasks` | [docs](https://developers.gobridgit.com/reference/accounts_querytasks) |
| [List Account User Profiles](actions/list-account-user-profiles.md) | `GET /rp/api/v1/Accounts/:id/user-profiles` | [docs](https://developers.gobridgit.com/reference/accounts_queryuserprofiles) |
| [List Account Users](actions/list-account-users.md) | `GET /rp/api/v1/accounts/:accountId/users` | [docs](https://developers.gobridgit.com/reference/accountusers_query) |
| [List Accounts](actions/list-accounts.md) | `GET /rp/api/v1/Accounts` | [docs](https://developers.gobridgit.com/reference/accounts_query) |
| [List Current Hourly Person Projects](actions/list-current-hourly-person-projects.md) | `GET /rp/api/v1/accounts/:accountId/Persons/current-projects-hourly` | [docs](https://developers.gobridgit.com/reference/persons_getcurrentprojectshourly) |
| [List Current Person Projects](actions/list-current-person-projects.md) | `GET /rp/api/v1/accounts/:accountId/Persons/current-projects` | [docs](https://developers.gobridgit.com/reference/persons_getcurrentprojects) |
| [List Experience Field Candidates](actions/list-experience-field-candidates.md) | `GET /rp/api/v1/accounts/:accountId/experience-fields/candidates` | [docs](https://developers.gobridgit.com/reference/experiencefields_querycandidates) |
| [List Experience Field Values](actions/list-experience-field-values.md) | `GET /rp/api/v1/accounts/:accountId/experience-fields/:experienceFieldId/values` | [docs](https://developers.gobridgit.com/reference/experiencefieldvalues_query) |
| [List Experience Fields](actions/list-experience-fields.md) | `GET /rp/api/v1/accounts/:accountId/experience-fields` | [docs](https://developers.gobridgit.com/reference/experiencefields_query) |
| [List Hourly Allocations](actions/list-hourly-allocations.md) | `GET /rp/api/v1/accounts/:accountId/projects/:projectId/hourly-allocations` | [docs](https://developers.gobridgit.com/reference/hourlyallocations_query) |
| [List Hourly Role Names](actions/list-hourly-role-names.md) | `GET /rp/api/v1/accounts/:id/hourly-role-names` | [docs](https://developers.gobridgit.com/reference/hourlyrolenames_get) |
| [List People](actions/list-people.md) | `GET /rp/api/v1/accounts/:accountId/Persons` | [docs](https://developers.gobridgit.com/reference/persons_query) |
| [List Person Allocations](actions/list-person-allocations.md) | `GET /rp/api/v1/accounts/:accountId/Persons/:id/allocations` | [docs](https://developers.gobridgit.com/reference/persons_getallocations) |
| [List Person Attachments](actions/list-person-attachments.md) | `GET /rp/api/v1/accounts/:accountId/persons/:personId/attachments` | [docs](https://developers.gobridgit.com/reference/personattachments_query) |
| [List Person Availabilities](actions/list-person-availabilities.md) | `GET /rp/api/v1/accounts/:accountId/Persons/availabilities` | [docs](https://developers.gobridgit.com/reference/persons_querynextavailables) |
| [List Person Certification Attachments](actions/list-person-certification-attachments.md) | `GET /rp/api/v1/accounts/:accountId/persons/:personId/certifications/:certId/attachments` | [docs](https://developers.gobridgit.com/reference/personcertattachments_query) |
| [List Person Certifications](actions/list-person-certifications.md) | `GET /rp/api/v1/accounts/:accountId/persons/:personId/certifications` | [docs](https://developers.gobridgit.com/reference/personcertifications_query) |
| [List Person Field Values](actions/list-person-field-values.md) | `GET /rp/api/v1/accounts/:accountId/persons/:personId/person-field-values` | [docs](https://developers.gobridgit.com/reference/personfieldvalue_queryfieldvalues) |
| [List Person Fields](actions/list-person-fields.md) | `GET /rp/api/v1/accounts/:id/person-fields` | [docs](https://developers.gobridgit.com/reference/personfields_query) |
| [List Person Historical Experiences](actions/list-person-historical-experiences.md) | `GET /rp/api/v1/accounts/:accountId/persons/:personId/historical-experiences` | [docs](https://developers.gobridgit.com/reference/personhistoricalexperiences_getall) |
| [List Person Projects](actions/list-person-projects.md) | `GET /rp/api/v1/accounts/:accountId/Persons/:id/projects` | [docs](https://developers.gobridgit.com/reference/persons_getprojects) |
| [List Person Unavailabilities](actions/list-person-unavailabilities.md) | `GET /rp/api/v1/accounts/:accountId/persons/:id/unavailabilities` | [docs](https://developers.gobridgit.com/reference/personunavailabilities_getunavailabilities) |
| [List Project Allocations](actions/list-project-allocations.md) | `GET /rp/api/v1/accounts/:accountId/projects/:projectId/Allocations` | [docs](https://developers.gobridgit.com/reference/allocations_query) |
| [List Project Field Values](actions/list-project-field-values.md) | `GET /rp/api/v1/accounts/:accountId/projects/:projectId/project-field-values` | [docs](https://developers.gobridgit.com/reference/projectfieldvalue_queryfieldvalues) |
| [List Project Fields](actions/list-project-fields.md) | `GET /rp/api/v1/accounts/:id/project-fields` | [docs](https://developers.gobridgit.com/reference/projectfields_query) |
| [List Project Notes](actions/list-project-notes.md) | `GET /rp/api/v1/accounts/:accountId/projects/:projectId/notes` | [docs](https://developers.gobridgit.com/reference/projectnotes_query) |
| [List Project Phases](actions/list-project-phases.md) | `GET /rp/api/v1/accounts/:accountId/projects/:projectId/phases` | [docs](https://developers.gobridgit.com/reference/projectsphases_query) |
| [List Project Role Categories](actions/list-project-role-categories.md) | `GET /rp/api/v1/accounts/:accountId/projects/:projectId/role-categories` | [docs](https://developers.gobridgit.com/reference/projectrolecategories_query) |
| [List Project Roles](actions/list-project-roles.md) | `GET /rp/api/v1/accounts/:accountId/projects/:projectId/roles` | [docs](https://developers.gobridgit.com/reference/projectroles_query) |
| [List Projects](actions/list-projects.md) | `GET /rp/api/v1/accounts/:accountId/Projects` | [docs](https://developers.gobridgit.com/reference/projects_query) |
| [List Role Names](actions/list-role-names.md) | `GET /rp/api/v1/accounts/:accountId/role-names` | [docs](https://developers.gobridgit.com/reference/rolenames_get) |
| [List Saved Filters](actions/list-saved-filters.md) | `GET /rp/api/v1/accounts/:accountId/my-filters` | [docs](https://developers.gobridgit.com/reference/userfilters_query) |
| [List Service Accounts](actions/list-service-accounts.md) | `GET /rp/api/v1/accounts/:accountId/service-accounts` | [docs](https://developers.gobridgit.com/reference/serviceaccounts_getserviceaccounts) |
| [Patch Person Historical Experience](actions/patch-person-historical-experience.md) | `PATCH /rp/api/v1/accounts/:accountId/persons/:personId/historical-experiences/:historicalExperienceId` | [docs](https://developers.gobridgit.com/reference/personhistoricalexperiences_patch) |
| [Promote Custom Fields to Experience Fields](actions/promote-custom-fields-to-experience-fields.md) | `POST /rp/api/v1/accounts/:accountId/experience-fields` | [docs](https://developers.gobridgit.com/reference/experiencefields_promotecustomfields) |
| [Reactivate Person](actions/reactivate-person.md) | `POST /rp/api/v1/accounts/:accountId/Persons/:id/restore` | [docs](https://developers.gobridgit.com/reference/persons_restore) |
| [Remove Project Task Role Allocation](actions/remove-project-task-role-allocation.md) | `DELETE /rp/api/v1/accounts/:accountId/projects/:projectId/tasks/:taskId/roles/:id/allocations` | [docs](https://developers.gobridgit.com/reference/projecttasks_removeallocation) |
| [Reorder Person Fields](actions/reorder-person-fields.md) | `PUT /rp/api/v1/accounts/:id/person-fields/_reorder` | [docs](https://developers.gobridgit.com/reference/personfields_updatefieldorder) |
| [Reorder Project Fields](actions/reorder-project-fields.md) | `PUT /rp/api/v1/accounts/:id/project-fields/_reorder` | [docs](https://developers.gobridgit.com/reference/projectfields_updatefieldorder) |
| [Reset Account User Authentication Method](actions/reset-account-user-authentication-method.md) | `POST /rp/api/v1/accounts/:accountId/users/:userId/reset-auth-method` | [docs](https://developers.gobridgit.com/reference/accountusers_resetauthmethod) |
| [Reset Service Account Password](actions/reset-service-account-password.md) | `POST /rp/api/v1/accounts/:accountId/service-accounts/:id/reset-password` | [docs](https://developers.gobridgit.com/reference/serviceaccounts_resetpassword) |
| [Search Account Activities](actions/search-account-activities.md) | `POST /rp/api/v1/accounts/:accountId/activities/_filter` | [docs](https://developers.gobridgit.com/reference/accountactivities_filter) |
| [Search Accounts](actions/search-accounts.md) | `POST /rp/api/v1/Accounts/_filter` | [docs](https://developers.gobridgit.com/reference/accounts_queryfilter) |
| [Search People](actions/search-people.md) | `POST /rp/api/v1/accounts/:accountId/Persons/_filter` | [docs](https://developers.gobridgit.com/reference/persons_queryfilter) |
| [Search Person Collaborations](actions/search-person-collaborations.md) | `POST /rp/api/v1/Accounts/:id/collaboration-matrix/_filter` | [docs](https://developers.gobridgit.com/reference/accounts_querycollaborationmatrix) |
| [Search Projects](actions/search-projects.md) | `POST /rp/api/v1/accounts/:accountId/Projects/_filter` | [docs](https://developers.gobridgit.com/reference/projects_queryfilter) |
| [Send Account Invitation](actions/send-account-invitation.md) | `POST /rp/api/v1/accounts/:accountId/invitations` | [docs](https://developers.gobridgit.com/reference/accountinvitations_post) |
| [Set Account User Permission Group](actions/set-account-user-permission-group.md) | `PUT /rp/api/v1/accounts/:accountId/users/:id/membership` | [docs](https://developers.gobridgit.com/reference/accountusers_setmembership) |
| [Set Hourly Role Names](actions/set-hourly-role-names.md) | `POST /rp/api/v1/accounts/:id/hourly-role-names` | [docs](https://developers.gobridgit.com/reference/hourlyrolenames_post) |
| [Set Person External ID](actions/set-person-external-id.md) | `PUT /rp/api/v1/accounts/:accountId/Persons/:id/externalId` | [docs](https://developers.gobridgit.com/reference/persons_setexternalid) |
| [Set Person Field Values](actions/set-person-field-values.md) | `POST /rp/api/v1/accounts/:accountId/persons/:personId/person-field-values` | [docs](https://developers.gobridgit.com/reference/personfieldvalue_setfieldvalues) |
| [Set Person Fields](actions/set-person-fields.md) | `POST /rp/api/v1/accounts/:id/person-fields` | [docs](https://developers.gobridgit.com/reference/personfields_post) |
| [Set Person Groupings](actions/set-person-groupings.md) | `POST /rp/api/v1/accounts/:accountId/persons/:personId/groupings` | [docs](https://developers.gobridgit.com/reference/persongroupings_set) |
| [Set Person Profile Picture](actions/set-person-profile-picture.md) | `PUT /rp/api/v1/accounts/:accountId/persons/:personId/profile-picture` | [docs](https://developers.gobridgit.com/reference/personprofile_put) |
| [Set Project External ID](actions/set-project-external-id.md) | `PUT /rp/api/v1/accounts/:accountId/Projects/:id/externalId` | [docs](https://developers.gobridgit.com/reference/projects_putexternalid) |
| [Set Project Field Values](actions/set-project-field-values.md) | `POST /rp/api/v1/accounts/:accountId/projects/:projectId/project-field-values` | [docs](https://developers.gobridgit.com/reference/projectfieldvalue_setfieldvalues) |
| [Set Project Fields](actions/set-project-fields.md) | `POST /rp/api/v1/accounts/:id/project-fields` | [docs](https://developers.gobridgit.com/reference/projectfields_post) |
| [Set Project Groupings](actions/set-project-groupings.md) | `POST /rp/api/v1/accounts/:accountId/projects/:projectId/groupings` | [docs](https://developers.gobridgit.com/reference/projectgroupings_set) |
| [Set Project Role External ID](actions/set-project-role-external-id.md) | `PUT /rp/api/v1/accounts/:accountId/projects/:projectId/roles/:id/externalId` | [docs](https://developers.gobridgit.com/reference/projectroles_setexternalid) |
| [Set Role Names](actions/set-role-names.md) | `POST /rp/api/v1/accounts/:accountId/role-names` | [docs](https://developers.gobridgit.com/reference/rolenames_post) |
| [Set User Permission Group](actions/set-user-permission-group.md) | `PUT /rp/api/v1/Users/:id/membership` | [docs](https://developers.gobridgit.com/reference/users_setmembership) |
| [Update Account Certification](actions/update-account-certification.md) | `PATCH /rp/api/v1/accounts/:accountId/certifications/:id` | [docs](https://developers.gobridgit.com/reference/accountcertifications_update) |
| [Update Account Grouping](actions/update-account-grouping.md) | `PATCH /rp/api/v1/accounts/:accountId/groupings/:id` | [docs](https://developers.gobridgit.com/reference/accountgroupings_update) |
| [Update Account Phase](actions/update-account-phase.md) | `PUT /rp/api/v1/accounts/:accountId/Phases/:id` | [docs](https://developers.gobridgit.com/reference/phases_updatesingle) |
| [Update Account Phases](actions/update-account-phases.md) | `PUT /rp/api/v1/accounts/:accountId/Phases` | [docs](https://developers.gobridgit.com/reference/phases_update) |
| [Update Account User](actions/update-account-user.md) | `PATCH /rp/api/v1/accounts/:accountId/users/:id` | [docs](https://developers.gobridgit.com/reference/accountusers_patch) |
| [Update Experience Field Value](actions/update-experience-field-value.md) | `POST /rp/api/v1/accounts/:accountId/experience-fields/:experienceFieldId/values/:experienceFieldValueId` | [docs](https://developers.gobridgit.com/reference/experiencefieldvalues_update) |
| [Update Hourly Allocation](actions/update-hourly-allocation.md) | `PUT /rp/api/v1/accounts/:accountId/projects/:projectId/hourly-allocations` | [docs](https://developers.gobridgit.com/reference/hourlyallocations_put) |
| [Update Hourly Allocation Segment](actions/update-hourly-allocation-segment.md) | `PUT /rp/api/v1/accounts/:accountId/projects/:projectId/hourly-allocations/:id` | [docs](https://developers.gobridgit.com/reference/hourlyallocations_putbyid) |
| [Update Person](actions/update-person.md) | `PATCH /rp/api/v1/accounts/:accountId/Persons/:id` | [docs](https://developers.gobridgit.com/reference/persons_update) |
| [Update Person Certification](actions/update-person-certification.md) | `PUT /rp/api/v1/accounts/:accountId/persons/:personId/certifications/:id` | [docs](https://developers.gobridgit.com/reference/personcertifications_update) |
| [Update Person Employment Period](actions/update-person-employment-period.md) | `PATCH /rp/api/v1/accounts/:accountId/persons/:personId/employment-periods/:periodId` | [docs](https://developers.gobridgit.com/reference/personemploymentperiods_update) |
| [Update Person Field Value](actions/update-person-field-value.md) | `PATCH /rp/api/v1/accounts/:accountId/persons/:personId/person-field-values/:fieldId` | [docs](https://developers.gobridgit.com/reference/personfieldvalue_updatefieldvalue) |
| [Update Person Field Values](actions/update-person-field-values.md) | `PATCH /rp/api/v1/accounts/:accountId/persons/:personId/person-field-values` | [docs](https://developers.gobridgit.com/reference/personfieldvalue_bulkupdatefieldvalues) |
| [Update Person Groupings](actions/update-person-groupings.md) | `PUT /rp/api/v1/accounts/:accountId/persons/:personId/groupings` | [docs](https://developers.gobridgit.com/reference/persongroupings_put) |
| [Update Person Historical Experience](actions/update-person-historical-experience.md) | `PUT /rp/api/v1/accounts/:accountId/persons/:personId/historical-experiences/:historicalExperienceId` | [docs](https://developers.gobridgit.com/reference/personhistoricalexperiences_update) |
| [Update Person Historical Experience Field](actions/update-person-historical-experience-field.md) | `PATCH /rp/api/v1/accounts/:accountId/persons/:personId/historical-experiences/:historicalExperienceId/experience-fields/:experienceFieldId` | [docs](https://developers.gobridgit.com/reference/personhistoricalexperiencefields_patch) |
| [Update Person Title](actions/update-person-title.md) | `PATCH /rp/api/v1/accounts/:accountId/persons/:personId/titles/:entryId` | [docs](https://developers.gobridgit.com/reference/persontitles_update) |
| [Update Person Unavailabilities](actions/update-person-unavailabilities.md) | `PATCH /rp/api/v1/accounts/:accountId/persons/:id/unavailabilities` | [docs](https://developers.gobridgit.com/reference/personunavailabilities_updateunavailabilities) |
| [Update Project](actions/update-project.md) | `PATCH /rp/api/v1/accounts/:accountId/Projects/:id` | [docs](https://developers.gobridgit.com/reference/projects_update) |
| [Update Project Allocation](actions/update-project-allocation.md) | `PUT /rp/api/v1/accounts/:accountId/projects/:projectId/Allocations` | [docs](https://developers.gobridgit.com/reference/allocations_put) |
| [Update Project Allocation Segment](actions/update-project-allocation-segment.md) | `PUT /rp/api/v1/accounts/:accountId/projects/:projectId/Allocations/:id` | [docs](https://developers.gobridgit.com/reference/allocations_putbyid) |
| [Update Project Field Value](actions/update-project-field-value.md) | `PATCH /rp/api/v1/accounts/:accountId/projects/:projectId/project-field-values/:fieldId` | [docs](https://developers.gobridgit.com/reference/projectfieldvalue_updatefieldvalue) |
| [Update Project Field Values](actions/update-project-field-values.md) | `PATCH /rp/api/v1/accounts/:accountId/projects/:projectId/project-field-values` | [docs](https://developers.gobridgit.com/reference/projectfieldvalue_bulkupdatefieldvalues) |
| [Update Project Groupings](actions/update-project-groupings.md) | `PUT /rp/api/v1/accounts/:accountId/projects/:projectId/groupings` | [docs](https://developers.gobridgit.com/reference/projectgroupings_put) |
| [Update Project Note](actions/update-project-note.md) | `PATCH /rp/api/v1/accounts/:accountId/projects/:projectId/notes/:id` | [docs](https://developers.gobridgit.com/reference/projectnotes_update) |
| [Update Project Phase](actions/update-project-phase.md) | `PUT /rp/api/v1/accounts/:accountId/projects/:projectId/phases/:phaseId` | [docs](https://developers.gobridgit.com/reference/projectsphases_update) |
| [Update Project Phases in Bulk](actions/update-project-phases-in-bulk.md) | `PUT /rp/api/v1/accounts/:accountId/projects/:projectId/phases/bulk` | [docs](https://developers.gobridgit.com/reference/projectsphases_bulkupdate) |
| [Update Project Role](actions/update-project-role.md) | `PUT /rp/api/v1/accounts/:accountId/projects/:projectId/roles/:id` | [docs](https://developers.gobridgit.com/reference/projectroles_update) |
| [Update Project Role Categories](actions/update-project-role-categories.md) | `PUT /rp/api/v1/accounts/:accountId/projects/:projectId/role-categories` | [docs](https://developers.gobridgit.com/reference/projectrolecategories_update) |
| [Update Project Roles in Bulk](actions/update-project-roles-in-bulk.md) | `PATCH /rp/api/v1/accounts/:accountId/projects/:projectId/roles/bulk` | [docs](https://developers.gobridgit.com/reference/projectroles_bulkpatchupdate) |
| [Update Project Task Role](actions/update-project-task-role.md) | `PATCH /rp/api/v1/accounts/:accountId/projects/:projectId/tasks/:taskId/roles/:id` | [docs](https://developers.gobridgit.com/reference/projecttasks_updaterole) |
| [Update Project Tasks](actions/update-project-tasks.md) | `PUT /rp/api/v1/accounts/:accountId/projects/:projectId/tasks` | [docs](https://developers.gobridgit.com/reference/projecttasks_update) |
| [Update Saved Filter](actions/update-saved-filter.md) | `PATCH /rp/api/v1/accounts/:accountId/my-filters/:id` | [docs](https://developers.gobridgit.com/reference/userfilters_update) |
| [Update Service Account](actions/update-service-account.md) | `PUT /rp/api/v1/accounts/:accountId/service-accounts/:id` | [docs](https://developers.gobridgit.com/reference/serviceaccounts_updateserviceaccount) |
