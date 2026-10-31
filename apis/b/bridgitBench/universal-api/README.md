# <img src="https://images.mindcloud.co/apps/icons/bridgit-bench_1789766868963.png" alt="Bridgit Bench logo" width="28" height="28"> Bridgit Bench: Universal API

Manage people, projects, staffing allocations, and workforce availability

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/bridgitBench/latest
- **Category:** Productivity / Project Management
- **Actions:** 200
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://gobridgit.com
- **Vendor API docs:** https://developers.gobridgit.com/reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Accounts](actions/list-accounts.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bridgitBench/latest/actions/list-accounts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (200)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Get Account](actions/get-account.md) | GET |  |
| [List Account Hourly Roles](actions/list-account-hourly-roles.md) | GET |  |
| [List Account Person Certifications](actions/list-account-person-certifications.md) | GET |  |
| [List Account Person Field Values](actions/list-account-person-field-values.md) | GET |  |
| [List Account Project Field Values](actions/list-account-project-field-values.md) | GET |  |
| [List Account Role Categories](actions/list-account-role-categories.md) | GET |  |
| [List Account Salaried Roles](actions/list-account-salaried-roles.md) | GET |  |
| [List Account Tasks](actions/list-account-tasks.md) | GET |  |
| [List Account User Profiles](actions/list-account-user-profiles.md) | GET |  |
| [List Accounts](actions/list-accounts.md) | GET |  |
| [Search Accounts](actions/search-accounts.md) | GET |  |
| [Search Person Collaborations](actions/search-person-collaborations.md) | GET |  |

### Account Activity

| Action | Method | Description |
| --- | --- | --- |
| [Search Account Activities](actions/search-account-activities.md) | GET |  |

### Account Certification

| Action | Method | Description |
| --- | --- | --- |
| [Create Account Certification](actions/create-account-certification.md) | POST |  |
| [Delete Account Certification](actions/delete-account-certification.md) | DELETE |  |
| [Get Account Certification](actions/get-account-certification.md) | GET |  |
| [List Account Certifications](actions/list-account-certifications.md) | GET |  |
| [Update Account Certification](actions/update-account-certification.md) | PUT |  |

### Account Grouping

| Action | Method | Description |
| --- | --- | --- |
| [Create Account Grouping](actions/create-account-grouping.md) | POST |  |
| [Delete Account Grouping](actions/delete-account-grouping.md) | DELETE |  |
| [Get Account Grouping](actions/get-account-grouping.md) | GET |  |
| [List Account Groupings](actions/list-account-groupings.md) | GET |  |
| [Update Account Grouping](actions/update-account-grouping.md) | PUT |  |

### Account Integration

| Action | Method | Description |
| --- | --- | --- |
| [Get Account Integration](actions/get-account-integration.md) | GET |  |

### Account Invitation

| Action | Method | Description |
| --- | --- | --- |
| [Delete Account Invitation](actions/delete-account-invitation.md) | DELETE |  |
| [List Account Invitations](actions/list-account-invitations.md) | GET |  |
| [Send Account Invitation](actions/send-account-invitation.md) | POST |  |

### Account Phase

| Action | Method | Description |
| --- | --- | --- |
| [Create Account Phase](actions/create-account-phase.md) | POST |  |
| [Delete Account Phases](actions/delete-account-phases.md) | DELETE |  |
| [Get Account Phase](actions/get-account-phase.md) | GET |  |
| [List Account Phases](actions/list-account-phases.md) | GET |  |
| [Update Account Phase](actions/update-account-phase.md) | PUT |  |
| [Update Account Phases](actions/update-account-phases.md) | PUT |  |

### Account User

| Action | Method | Description |
| --- | --- | --- |
| [Deactivate Account User](actions/deactivate-account-user.md) | DELETE |  |
| [Get Account User](actions/get-account-user.md) | GET |  |
| [List Account Users](actions/list-account-users.md) | GET |  |
| [Reset Account User Authentication Method](actions/reset-account-user-authentication-method.md) | PUT |  |
| [Set Account User Permission Group](actions/set-account-user-permission-group.md) | PUT |  |
| [Update Account User](actions/update-account-user.md) | PUT |  |

### Experience Field

| Action | Method | Description |
| --- | --- | --- |
| [Demote Experience Field](actions/demote-experience-field.md) | DELETE |  |
| [List Experience Field Candidates](actions/list-experience-field-candidates.md) | GET |  |
| [List Experience Fields](actions/list-experience-fields.md) | GET |  |
| [Promote Custom Fields to Experience Fields](actions/promote-custom-fields-to-experience-fields.md) | PUT |  |

### Experience Field Value

| Action | Method | Description |
| --- | --- | --- |
| [Create Experience Field Values](actions/create-experience-field-values.md) | POST |  |
| [Delete Experience Field Value](actions/delete-experience-field-value.md) | DELETE |  |
| [List Experience Field Values](actions/list-experience-field-values.md) | GET |  |
| [Update Experience Field Value](actions/update-experience-field-value.md) | PUT |  |

### External Record

| Action | Method | Description |
| --- | --- | --- |
| [Get Person by External ID](actions/get-person-by-external-id.md) | GET |  |
| [Get Project by External ID](actions/get-project-by-external-id.md) | GET |  |
| [Get Project Role by External ID](actions/get-project-role-by-external-id.md) | GET |  |

### Hourly Allocation

| Action | Method | Description |
| --- | --- | --- |
| [Create Hourly Allocation](actions/create-hourly-allocation.md) | POST |  |
| [Delete Hourly Allocation](actions/delete-hourly-allocation.md) | DELETE |  |
| [List Hourly Allocations](actions/list-hourly-allocations.md) | GET |  |
| [Update Hourly Allocation](actions/update-hourly-allocation.md) | PUT |  |
| [Update Hourly Allocation Segment](actions/update-hourly-allocation-segment.md) | PUT |  |

### Hourly Role Name

| Action | Method | Description |
| --- | --- | --- |
| [Delete Hourly Role Names](actions/delete-hourly-role-names.md) | DELETE |  |
| [List Hourly Role Names](actions/list-hourly-role-names.md) | GET |  |
| [Set Hourly Role Names](actions/set-hourly-role-names.md) | PUT |  |

### Person

| Action | Method | Description |
| --- | --- | --- |
| [Create Person](actions/create-person.md) | POST |  |
| [Deactivate Person](actions/deactivate-person.md) | DELETE |  |
| [Deactivate Person with Details](actions/deactivate-person-with-details.md) | PUT |  |
| [Get Person](actions/get-person.md) | GET |  |
| [List Current Hourly Person Projects](actions/list-current-hourly-person-projects.md) | GET |  |
| [List Current Person Projects](actions/list-current-person-projects.md) | GET |  |
| [List People](actions/list-people.md) | GET |  |
| [List Person Allocations](actions/list-person-allocations.md) | GET |  |
| [List Person Availabilities](actions/list-person-availabilities.md) | GET |  |
| [List Person Projects](actions/list-person-projects.md) | GET |  |
| [Reactivate Person](actions/reactivate-person.md) | PUT |  |
| [Search People](actions/search-people.md) | GET |  |
| [Set Person External ID](actions/set-person-external-id.md) | PUT |  |
| [Update Person](actions/update-person.md) | PUT |  |

### Person Attachment

| Action | Method | Description |
| --- | --- | --- |
| [Create Person Attachment](actions/create-person-attachment.md) | POST |  |
| [Delete Person Attachment](actions/delete-person-attachment.md) | DELETE |  |
| [Get Person Attachment](actions/get-person-attachment.md) | GET |  |
| [List Person Attachments](actions/list-person-attachments.md) | GET |  |

### Person Certification

| Action | Method | Description |
| --- | --- | --- |
| [Create Person Certification](actions/create-person-certification.md) | POST |  |
| [Delete Person Certification](actions/delete-person-certification.md) | DELETE |  |
| [Get Person Certification](actions/get-person-certification.md) | GET |  |
| [List Person Certifications](actions/list-person-certifications.md) | GET |  |
| [Update Person Certification](actions/update-person-certification.md) | PUT |  |

### Person Certification Attachment

| Action | Method | Description |
| --- | --- | --- |
| [Delete Person Certification Attachment](actions/delete-person-certification-attachment.md) | DELETE |  |
| [Get Person Certification Attachment](actions/get-person-certification-attachment.md) | GET |  |
| [Link Person Certification Attachment](actions/link-person-certification-attachment.md) | POST |  |
| [List Person Certification Attachments](actions/list-person-certification-attachments.md) | GET |  |

### Person Employment Period

| Action | Method | Description |
| --- | --- | --- |
| [Create Person Employment Period](actions/create-person-employment-period.md) | POST |  |
| [Delete Person Employment Period](actions/delete-person-employment-period.md) | DELETE |  |
| [Get Person Employment History](actions/get-person-employment-history.md) | GET |  |
| [Update Person Employment Period](actions/update-person-employment-period.md) | PUT |  |

### Person Field

| Action | Method | Description |
| --- | --- | --- |
| [Delete Person Fields](actions/delete-person-fields.md) | DELETE |  |
| [List Person Fields](actions/list-person-fields.md) | GET |  |
| [Reorder Person Fields](actions/reorder-person-fields.md) | PUT |  |
| [Set Person Fields](actions/set-person-fields.md) | PUT |  |

### Person Field Value

| Action | Method | Description |
| --- | --- | --- |
| [Clear Person Field Values](actions/clear-person-field-values.md) | DELETE |  |
| [List Person Field Values](actions/list-person-field-values.md) | GET |  |
| [Set Person Field Values](actions/set-person-field-values.md) | PUT |  |
| [Update Person Field Value](actions/update-person-field-value.md) | PUT |  |
| [Update Person Field Values](actions/update-person-field-values.md) | PUT |  |

### Person Grouping

| Action | Method | Description |
| --- | --- | --- |
| [Delete Person Grouping](actions/delete-person-grouping.md) | DELETE |  |
| [Set Person Groupings](actions/set-person-groupings.md) | PUT |  |
| [Update Person Groupings](actions/update-person-groupings.md) | PUT |  |

### Person Historical Experience

| Action | Method | Description |
| --- | --- | --- |
| [Create Person Historical Experience](actions/create-person-historical-experience.md) | POST |  |
| [Delete Person Historical Experience](actions/delete-person-historical-experience.md) | DELETE |  |
| [Get Person Historical Experience](actions/get-person-historical-experience.md) | GET |  |
| [List Person Historical Experiences](actions/list-person-historical-experiences.md) | GET |  |
| [Patch Person Historical Experience](actions/patch-person-historical-experience.md) | PUT |  |
| [Update Person Historical Experience](actions/update-person-historical-experience.md) | PUT |  |

### Person Historical Experience Field

| Action | Method | Description |
| --- | --- | --- |
| [Create Person Historical Experience Field](actions/create-person-historical-experience-field.md) | POST |  |
| [Delete Person Historical Experience Field](actions/delete-person-historical-experience-field.md) | DELETE |  |
| [Update Person Historical Experience Field](actions/update-person-historical-experience-field.md) | PUT |  |

### Person Profile

| Action | Method | Description |
| --- | --- | --- |
| [Delete Person Profile Picture](actions/delete-person-profile-picture.md) | DELETE |  |
| [Get My Person Profile](actions/get-my-person-profile.md) | GET |  |
| [Set Person Profile Picture](actions/set-person-profile-picture.md) | PUT |  |

### Person Title

| Action | Method | Description |
| --- | --- | --- |
| [Create Person Title](actions/create-person-title.md) | POST |  |
| [Delete Person Title](actions/delete-person-title.md) | DELETE |  |
| [Get Person Title History](actions/get-person-title-history.md) | GET |  |
| [Update Person Title](actions/update-person-title.md) | PUT |  |

### Person Unavailability

| Action | Method | Description |
| --- | --- | --- |
| [Create Person Unavailabilities](actions/create-person-unavailabilities.md) | POST |  |
| [Delete Person Unavailabilities](actions/delete-person-unavailabilities.md) | DELETE |  |
| [List Account Person Unavailabilities](actions/list-account-person-unavailabilities.md) | GET |  |
| [List Person Unavailabilities](actions/list-person-unavailabilities.md) | GET |  |
| [Update Person Unavailabilities](actions/update-person-unavailabilities.md) | PUT |  |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [Create Project](actions/create-project.md) | POST |  |
| [Delete Project](actions/delete-project.md) | DELETE |  |
| [Get Project](actions/get-project.md) | GET |  |
| [List Projects](actions/list-projects.md) | GET |  |
| [Search Projects](actions/search-projects.md) | GET |  |
| [Set Project External ID](actions/set-project-external-id.md) | PUT |  |
| [Update Project](actions/update-project.md) | PUT |  |

### Project Allocation

| Action | Method | Description |
| --- | --- | --- |
| [Create Project Allocation](actions/create-project-allocation.md) | POST |  |
| [Delete Project Allocation](actions/delete-project-allocation.md) | DELETE |  |
| [List Project Allocations](actions/list-project-allocations.md) | GET |  |
| [Update Project Allocation](actions/update-project-allocation.md) | PUT |  |
| [Update Project Allocation Segment](actions/update-project-allocation-segment.md) | PUT |  |

### Project Field

| Action | Method | Description |
| --- | --- | --- |
| [Delete Project Fields](actions/delete-project-fields.md) | DELETE |  |
| [List Project Fields](actions/list-project-fields.md) | GET |  |
| [Reorder Project Fields](actions/reorder-project-fields.md) | PUT |  |
| [Set Project Fields](actions/set-project-fields.md) | PUT |  |

### Project Field Value

| Action | Method | Description |
| --- | --- | --- |
| [Clear Project Field Values](actions/clear-project-field-values.md) | DELETE |  |
| [List Project Field Values](actions/list-project-field-values.md) | GET |  |
| [Set Project Field Values](actions/set-project-field-values.md) | PUT |  |
| [Update Project Field Value](actions/update-project-field-value.md) | PUT |  |
| [Update Project Field Values](actions/update-project-field-values.md) | PUT |  |

### Project Grouping

| Action | Method | Description |
| --- | --- | --- |
| [Delete Project Grouping](actions/delete-project-grouping.md) | DELETE |  |
| [Set Project Groupings](actions/set-project-groupings.md) | PUT |  |
| [Update Project Groupings](actions/update-project-groupings.md) | PUT |  |

### Project Note

| Action | Method | Description |
| --- | --- | --- |
| [Create Project Note](actions/create-project-note.md) | POST |  |
| [Delete Project Note](actions/delete-project-note.md) | DELETE |  |
| [Get Project Note](actions/get-project-note.md) | GET |  |
| [List Project Notes](actions/list-project-notes.md) | GET |  |
| [Update Project Note](actions/update-project-note.md) | PUT |  |

### Project Phase

| Action | Method | Description |
| --- | --- | --- |
| [Create Project Phase](actions/create-project-phase.md) | POST |  |
| [Create Project Phases in Bulk](actions/create-project-phases-in-bulk.md) | POST |  |
| [Delete Project Phase](actions/delete-project-phase.md) | DELETE |  |
| [Delete Project Phases in Bulk](actions/delete-project-phases-in-bulk.md) | DELETE |  |
| [List Project Phases](actions/list-project-phases.md) | GET |  |
| [Update Project Phase](actions/update-project-phase.md) | PUT |  |
| [Update Project Phases in Bulk](actions/update-project-phases-in-bulk.md) | PUT |  |

### Project Role

| Action | Method | Description |
| --- | --- | --- |
| [Create Project Role](actions/create-project-role.md) | POST |  |
| [Create Project Roles in Bulk](actions/create-project-roles-in-bulk.md) | POST |  |
| [Delete Project Role](actions/delete-project-role.md) | DELETE |  |
| [Delete Project Roles in Bulk](actions/delete-project-roles-in-bulk.md) | DELETE |  |
| [Get Project Role](actions/get-project-role.md) | GET |  |
| [List Project Roles](actions/list-project-roles.md) | GET |  |
| [Set Project Role External ID](actions/set-project-role-external-id.md) | PUT |  |
| [Update Project Role](actions/update-project-role.md) | PUT |  |
| [Update Project Roles in Bulk](actions/update-project-roles-in-bulk.md) | PUT |  |

### Project Role Category

| Action | Method | Description |
| --- | --- | --- |
| [Create Project Role Categories](actions/create-project-role-categories.md) | POST |  |
| [Delete Project Role Categories](actions/delete-project-role-categories.md) | DELETE |  |
| [List Project Role Categories](actions/list-project-role-categories.md) | GET |  |
| [Update Project Role Categories](actions/update-project-role-categories.md) | PUT |  |

### Project Task

| Action | Method | Description |
| --- | --- | --- |
| [Create Project Task Role](actions/create-project-task-role.md) | POST |  |
| [Create Project Task Role Allocation](actions/create-project-task-role-allocation.md) | POST |  |
| [Create Project Task Role Allocations in Bulk](actions/create-project-task-role-allocations-in-bulk.md) | POST |  |
| [Create Project Task Roles in Bulk](actions/create-project-task-roles-in-bulk.md) | POST |  |
| [Create Project Tasks](actions/create-project-tasks.md) | POST |  |
| [Create Project Tasks from Templates](actions/create-project-tasks-from-templates.md) | POST |  |
| [Delete Project Task](actions/delete-project-task.md) | DELETE |  |
| [Delete Project Task Role](actions/delete-project-task-role.md) | DELETE |  |
| [Remove Project Task Role Allocation](actions/remove-project-task-role-allocation.md) | DELETE |  |
| [Update Project Task Role](actions/update-project-task-role.md) | PUT |  |
| [Update Project Tasks](actions/update-project-tasks.md) | PUT |  |

### Role Allocation

| Action | Method | Description |
| --- | --- | --- |
| [Create Role Allocation](actions/create-role-allocation.md) | POST |  |

### Role Name

| Action | Method | Description |
| --- | --- | --- |
| [Delete Role Names](actions/delete-role-names.md) | DELETE |  |
| [List Role Names](actions/list-role-names.md) | GET |  |
| [Set Role Names](actions/set-role-names.md) | PUT |  |

### Saved Filter

| Action | Method | Description |
| --- | --- | --- |
| [Create Saved Filter](actions/create-saved-filter.md) | POST |  |
| [Delete Saved Filter](actions/delete-saved-filter.md) | DELETE |  |
| [Get Saved Filter](actions/get-saved-filter.md) | GET |  |
| [List Saved Filters](actions/list-saved-filters.md) | GET |  |
| [Update Saved Filter](actions/update-saved-filter.md) | PUT |  |

### Service Account

| Action | Method | Description |
| --- | --- | --- |
| [Create Service Account](actions/create-service-account.md) | POST |  |
| [Deactivate Service Account](actions/deactivate-service-account.md) | DELETE |  |
| [List Service Accounts](actions/list-service-accounts.md) | GET |  |
| [Reset Service Account Password](actions/reset-service-account-password.md) | PUT |  |
| [Update Service Account](actions/update-service-account.md) | PUT |  |

### Shared Filter

| Action | Method | Description |
| --- | --- | --- |
| [Delete Shared Filter](actions/delete-shared-filter.md) | DELETE |  |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Set User Permission Group](actions/set-user-permission-group.md) | PUT |  |

### Workforce Spend Report

| Action | Method | Description |
| --- | --- | --- |
| [Get Workforce Spend Hours Breakdown](actions/get-workforce-spend-hours-breakdown.md) | GET |  |
| [Get Workforce Spend Hours Overview](actions/get-workforce-spend-hours-overview.md) | GET |  |

