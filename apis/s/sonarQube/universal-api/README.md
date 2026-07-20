# <img src="https://images.mindcloud.co/apps/icons/sonarqube-icon_1776710480654.png" alt="SonarQube logo" width="28" height="28"> SonarQube: Universal API

SonarQube/SonarCloud code quality and security analysis API integration for projects, issues, measures, quality gates, users, groups, webhooks, and administration workflows.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/sonarQube/latest
- **Category:** IT Operations / Developer Tools
- **Actions:** 128
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.sonarsource.com/products/sonarqube/
- **Vendor API docs:** https://docs.sonarsource.com/sonarqube/latest/extension-guide/web-api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Validate Authentication](actions/validate-authentication.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sonarQube/latest/actions/validate-authentication?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (128)

### Authentication Session

| Action | Method | Description |
| --- | --- | --- |
| [Logout](actions/logout.md) | DELETE | Deletes the current SonarQube authentication session. |

### Authentication Validation

| Action | Method | Description |
| --- | --- | --- |
| [Validate Authentication](actions/validate-authentication.md) | GET | Retrieves SonarQube authentication validation results. |

### Component

| Action | Method | Description |
| --- | --- | --- |
| [List Component Tree](actions/list-component-tree.md) | GET | Retrieves a component tree from SonarQube. |
| [Search Components](actions/search-components.md) | GET | Finds components in SonarQube. |
| [Show Component](actions/show-component.md) | GET | Retrieves a component from SonarQube. |

### Component Measure

| Action | Method | Description |
| --- | --- | --- |
| [Get Component Measures](actions/get-component-measures.md) | GET | Retrieves component measures from SonarQube. |
| [List Component Measures](actions/list-component-measures.md) | GET | Retrieves component measures from SonarQube. |

### Compute Engine Activity Status

| Action | Method | Description |
| --- | --- | --- |
| [Get Compute Engine Activity Status](actions/get-compute-engine-activity-status.md) | GET | Retrieves compute engine activity status from SonarQube. |

### Compute Engine Component

| Action | Method | Description |
| --- | --- | --- |
| [Get Compute Engine Component](actions/get-compute-engine-component.md) | GET | Retrieves a compute engine component from SonarQube. |

### Compute Engine Task

| Action | Method | Description |
| --- | --- | --- |
| [Get Compute Engine Task](actions/get-compute-engine-task.md) | GET | Retrieves a compute engine task from SonarQube. |
| [Search Compute Engine Tasks](actions/search-compute-engine-tasks.md) | GET | Finds compute engine tasks in SonarQube. |

### Duplication

| Action | Method | Description |
| --- | --- | --- |
| [Show Duplications](actions/show-duplications.md) | GET | Retrieves duplications from SonarQube. |

### Favorite

| Action | Method | Description |
| --- | --- | --- |
| [Add Favorite](actions/add-favorite.md) | POST | Creates a favorite in SonarQube. |
| [Remove Favorite](actions/remove-favorite.md) | DELETE | Deletes a favorite from SonarQube. |
| [Search Favorites](actions/search-favorites.md) | GET | Finds favorites in SonarQube. |

### Issue

| Action | Method | Description |
| --- | --- | --- |
| [Assign Issue](actions/assign-issue.md) | PUT | Updates an issue assignee in SonarQube. |
| [Bulk Change Issues](actions/bulk-change-issues.md) | PUT | Updates multiple issues in SonarQube. |
| [Search Issues](actions/search-issues.md) | GET | Finds issues in SonarQube. |
| [Set Issue Tags](actions/set-issue-tags.md) | PUT | Updates issue tags in SonarQube. |
| [Transition Issue](actions/transition-issue.md) | PUT | Updates an issue transition in SonarQube. |

### Issue Author

| Action | Method | Description |
| --- | --- | --- |
| [List Issue Authors](actions/list-issue-authors.md) | GET | Retrieves issue authors from SonarQube. |

### Issue Changelog

| Action | Method | Description |
| --- | --- | --- |
| [Get Issue Changelog](actions/get-issue-changelog.md) | GET | Retrieves an issue changelog from SonarQube. |

### Issue Comment

| Action | Method | Description |
| --- | --- | --- |
| [Add Issue Comment](actions/add-issue-comment.md) | POST | Creates an issue comment in SonarQube. |
| [Delete Issue Comment](actions/delete-issue-comment.md) | DELETE | Deletes an issue comment from SonarQube. |
| [Edit Issue Comment](actions/edit-issue-comment.md) | PUT | Updates an issue comment in SonarQube. |

### Issue Tag

| Action | Method | Description |
| --- | --- | --- |
| [List Issue Tags](actions/list-issue-tags.md) | GET | Retrieves issue tags from SonarQube. |

### Language

| Action | Method | Description |
| --- | --- | --- |
| [List Languages](actions/list-languages.md) | GET | Retrieves languages from SonarQube. |

### Measure History

| Action | Method | Description |
| --- | --- | --- |
| [Search Measure History](actions/search-measure-history.md) | GET | Finds measure history in SonarQube. |

### Metric

| Action | Method | Description |
| --- | --- | --- |
| [Search Metrics](actions/search-metrics.md) | GET | Finds metrics in SonarQube. |

### Metric Type

| Action | Method | Description |
| --- | --- | --- |
| [List Metric Types](actions/list-metric-types.md) | GET | Retrieves metric types from SonarQube. |

### Notification

| Action | Method | Description |
| --- | --- | --- |
| [Add Notification](actions/add-notification.md) | POST | Creates a notification in SonarQube. |
| [List Notifications](actions/list-notifications.md) | GET | Retrieves notifications from SonarQube. |
| [Remove Notification](actions/remove-notification.md) | DELETE | Deletes a notification from SonarQube. |

### Permission

| Action | Method | Description |
| --- | --- | --- |
| [Add Group Permission](actions/add-group-permission.md) | POST | Creates a group permission in SonarQube. |
| [Add User Permission](actions/add-user-permission.md) | POST | Creates a user permission in SonarQube. |
| [Remove Group Permission](actions/remove-group-permission.md) | DELETE | Deletes a group permission from SonarQube. |
| [Remove User Permission](actions/remove-user-permission.md) | DELETE | Deletes a user permission from SonarQube. |

### Permission Template

| Action | Method | Description |
| --- | --- | --- |
| [Add Group To Permission Template](actions/add-group-to-permission-template.md) | POST | Adds a group to a SonarQube permission template. |
| [Add Project Creator To Permission Template](actions/add-project-creator-to-permission-template.md) | POST | Adds a project creator to a SonarQube permission template. |
| [Add User To Permission Template](actions/add-user-to-permission-template.md) | POST | Adds a user to a SonarQube permission template. |
| [Apply Permission Template](actions/apply-permission-template.md) | PUT | Updates a SonarQube project with a permission template. |
| [Bulk Apply Permission Template](actions/bulk-apply-permission-template.md) | PUT | Updates multiple SonarQube projects with a permission template. |
| [Create Permission Template](actions/create-permission-template.md) | POST | Creates a permission template in SonarQube. |
| [Delete Permission Template](actions/delete-permission-template.md) | DELETE | Deletes a permission template from SonarQube. |
| [Remove Group From Permission Template](actions/remove-group-from-permission-template.md) | DELETE | Removes a group from a SonarQube permission template. |
| [Remove Project Creator From Permission Template](actions/remove-project-creator-from-permission-template.md) | DELETE | Removes a project creator from a SonarQube permission template. |
| [Remove User From Permission Template](actions/remove-user-from-permission-template.md) | DELETE | Removes a user from a SonarQube permission template. |
| [Search Permission Templates](actions/search-permission-templates.md) | GET | Finds permission templates in SonarQube. |
| [Set Default Permission Template](actions/set-default-permission-template.md) | PUT | Updates the default permission template in SonarQube. |
| [Update Permission Template](actions/update-permission-template.md) | PUT | Updates a permission template in SonarQube. |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [Bulk Delete Projects](actions/bulk-delete-projects.md) | DELETE | Deletes multiple projects from SonarQube. |
| [Create Project](actions/create-project.md) | POST | Creates a project in SonarQube. |
| [Delete Project](actions/delete-project.md) | DELETE | Deletes a project from SonarQube. |
| [Search Projects](actions/search-projects.md) | GET | Finds projects in SonarQube. |
| [Update Project Key](actions/update-project-key.md) | PUT | Updates a project key in SonarQube. |
| [Update Project Visibility](actions/update-project-visibility.md) | PUT | Updates project visibility in SonarQube. |

### Project Analysis

| Action | Method | Description |
| --- | --- | --- |
| [Delete Project Analysis](actions/delete-project-analysis.md) | DELETE | Deletes a project analysis from SonarQube. |
| [Search Project Analyses](actions/search-project-analyses.md) | GET | Finds project analyses in SonarQube. |
| [Set Project Analysis Baseline](actions/set-project-analysis-baseline.md) | PUT | Updates a project analysis baseline in SonarQube. |
| [Unset Project Analysis Baseline](actions/unset-project-analysis-baseline.md) | PUT | Updates a project analysis baseline in SonarQube. |

### Project Analysis Event

| Action | Method | Description |
| --- | --- | --- |
| [Create Project Analysis Event](actions/create-project-analysis-event.md) | POST | Creates a project analysis event in SonarQube. |
| [Delete Project Analysis Event](actions/delete-project-analysis-event.md) | DELETE | Deletes a project analysis event from SonarQube. |
| [Update Project Analysis Event](actions/update-project-analysis-event.md) | PUT | Updates a project analysis event in SonarQube. |

### Project Badge

| Action | Method | Description |
| --- | --- | --- |
| [Get AI Code Assurance Badge](actions/get-ai-code-assurance-badge.md) | GET | Retrieves an AI code assurance badge from SonarQube. |
| [Get Project Measure Badge](actions/get-project-measure-badge.md) | GET | Retrieves a project measure badge from SonarQube. |
| [Get Project Quality Gate Badge](actions/get-project-quality-gate-badge.md) | GET | Retrieves a project quality gate badge from SonarQube. |

### Project Branch

| Action | Method | Description |
| --- | --- | --- |
| [Delete Project Branch](actions/delete-project-branch.md) | DELETE | Deletes a project branch from SonarQube. |
| [List Project Branches](actions/list-project-branches.md) | GET | Retrieves project branches from SonarQube. |
| [Rename Project Branch](actions/rename-project-branch.md) | PUT | Updates a project branch name in SonarQube. |

### Project Link

| Action | Method | Description |
| --- | --- | --- |
| [Create Project Link](actions/create-project-link.md) | POST | Creates a project link in SonarQube. |
| [Delete Project Link](actions/delete-project-link.md) | DELETE | Deletes a project link from SonarQube. |
| [Search Project Links](actions/search-project-links.md) | GET | Finds project links in SonarQube. |

### Project Pull Request

| Action | Method | Description |
| --- | --- | --- |
| [Delete Project Pull Request](actions/delete-project-pull-request.md) | DELETE | Deletes a project pull request from SonarQube. |
| [List Project Pull Requests](actions/list-project-pull-requests.md) | GET | Retrieves project pull requests from SonarQube. |

### Project Tag

| Action | Method | Description |
| --- | --- | --- |
| [Search Project Tags](actions/search-project-tags.md) | GET | Finds project tags in SonarQube. |
| [Set Project Tags](actions/set-project-tags.md) | PUT | Updates project tags in SonarQube. |

### Quality Profile

| Action | Method | Description |
| --- | --- | --- |
| [Change Quality Profile Parent](actions/change-quality-profile-parent.md) | PUT | Updates a quality profile parent in SonarQube. |
| [Copy Quality Profile](actions/copy-quality-profile.md) | POST | Creates a quality profile copy in SonarQube. |
| [Create Quality Profile](actions/create-quality-profile.md) | POST | Creates a quality profile in SonarQube. |
| [Delete Quality Profile](actions/delete-quality-profile.md) | DELETE | Deletes a quality profile from SonarQube. |
| [Rename Quality Profile](actions/rename-quality-profile.md) | PUT | Updates a quality profile name in SonarQube. |
| [Restore Quality Profile](actions/restore-quality-profile.md) | POST | Creates a restored quality profile in SonarQube. |
| [Search Quality Profiles](actions/search-quality-profiles.md) | GET | Finds quality profiles in SonarQube. |
| [Set Default Quality Profile](actions/set-default-quality-profile.md) | PUT | Updates the default quality profile in SonarQube. |

### Quality Profile Backup

| Action | Method | Description |
| --- | --- | --- |
| [Backup Quality Profile](actions/backup-quality-profile.md) | GET | Retrieves a quality profile backup from SonarQube. |

### Quality Profile Changelog

| Action | Method | Description |
| --- | --- | --- |
| [Get Quality Profile Changelog](actions/get-quality-profile-changelog.md) | GET | Retrieves a quality profile changelog from SonarQube. |

### Quality Profile Inheritance

| Action | Method | Description |
| --- | --- | --- |
| [Get Quality Profile Inheritance](actions/get-quality-profile-inheritance.md) | GET | Retrieves quality profile inheritance from SonarQube. |

### Quality Profile Project

| Action | Method | Description |
| --- | --- | --- |
| [Add Project To Quality Profile](actions/add-project-to-quality-profile.md) | POST | Adds a project to a SonarQube quality profile. |
| [List Quality Profile Projects](actions/list-quality-profile-projects.md) | GET | Retrieves projects for a quality profile in SonarQube. |
| [Remove Project From Quality Profile](actions/remove-project-from-quality-profile.md) | DELETE | Removes a project from a SonarQube quality profile. |

### Quality Profile Rule

| Action | Method | Description |
| --- | --- | --- |
| [Activate Quality Profile Rule](actions/activate-quality-profile-rule.md) | PUT | Updates a quality profile rule in SonarQube. |
| [Activate Quality Profile Rules](actions/activate-quality-profile-rules.md) | PUT | Updates multiple quality profile rules in SonarQube. |
| [Deactivate Quality Profile Rule](actions/deactivate-quality-profile-rule.md) | PUT | Updates a quality profile rule in SonarQube. |
| [Deactivate Quality Profile Rules](actions/deactivate-quality-profile-rules.md) | PUT | Updates multiple quality profile rules in SonarQube. |

### Rule

| Action | Method | Description |
| --- | --- | --- |
| [Search Rules](actions/search-rules.md) | GET | Finds rules in SonarQube. |
| [Show Rule](actions/show-rule.md) | GET | Retrieves a rule from SonarQube. |
| [Update Rule](actions/update-rule.md) | PUT | Updates a rule in SonarQube. |

### Rule Repository

| Action | Method | Description |
| --- | --- | --- |
| [List Rule Repositories](actions/list-rule-repositories.md) | GET | Retrieves rule repositories from SonarQube. |

### Rule Tag

| Action | Method | Description |
| --- | --- | --- |
| [List Rule Tags](actions/list-rule-tags.md) | GET | Retrieves rule tags from SonarQube. |

### Security Hotspot

| Action | Method | Description |
| --- | --- | --- |
| [Change Security Hotspot Status](actions/change-security-hotspot-status.md) | PUT | Updates a security hotspot status in SonarQube. |
| [Search Security Hotspots](actions/search-security-hotspots.md) | GET | Finds security hotspots in SonarQube. |
| [Show Security Hotspot](actions/show-security-hotspot.md) | GET | Retrieves a security hotspot from SonarQube. |

### Setting

| Action | Method | Description |
| --- | --- | --- |
| [Get Setting Values](actions/get-setting-values.md) | GET | Retrieves setting values from SonarQube. |
| [Reset Settings](actions/reset-settings.md) | PUT | Updates settings by resetting values in SonarQube. |
| [Set Setting](actions/set-setting.md) | PUT | Updates a setting in SonarQube. |

### Setting Definition

| Action | Method | Description |
| --- | --- | --- |
| [List Setting Definitions](actions/list-setting-definitions.md) | GET | Retrieves setting definitions from SonarQube. |

### Source File

| Action | Method | Description |
| --- | --- | --- |
| [Get Raw Source](actions/get-raw-source.md) | GET | Retrieves raw source from SonarQube. |
| [Show Source](actions/show-source.md) | GET | Retrieves source code from SonarQube. |

### Source Scm

| Action | Method | Description |
| --- | --- | --- |
| [Get Source SCM](actions/get-source-scm.md) | GET | Retrieves source SCM details from SonarQube. |

### User Group

| Action | Method | Description |
| --- | --- | --- |
| [Add User To Group](actions/add-user-to-group.md) | POST | Adds a user to a SonarQube user group. |
| [Create User Group](actions/create-user-group.md) | POST | Creates a user group in SonarQube. |
| [Delete User Group](actions/delete-user-group.md) | DELETE | Deletes a user group from SonarQube. |
| [List User Groups For User](actions/list-user-groups-for-user.md) | GET | Retrieves user groups for a SonarQube user. |
| [Remove User From Group](actions/remove-user-from-group.md) | DELETE | Removes a user from a SonarQube user group. |
| [Search User Groups](actions/search-user-groups.md) | GET | Finds user groups in SonarQube. |
| [Update User Group](actions/update-user-group.md) | PUT | Updates a user group in SonarQube. |

### User Group Member

| Action | Method | Description |
| --- | --- | --- |
| [List User Group Members](actions/list-user-group-members.md) | GET | Retrieves members of a SonarQube user group. |

### User Token

| Action | Method | Description |
| --- | --- | --- |
| [Generate User Token](actions/generate-user-token.md) | POST | Creates a user token in SonarQube. |
| [List User Tokens](actions/list-user-tokens.md) | GET | Retrieves user tokens from SonarQube. |
| [Revoke User Token](actions/revoke-user-token.md) | DELETE | Deletes a user token from SonarQube. |

### Web Api Endpoint

| Action | Method | Description |
| --- | --- | --- |
| [List Web API Endpoints](actions/list-web-api-endpoints.md) | GET | Retrieves Web API endpoints from SonarQube. |

### Web Api Response Example

| Action | Method | Description |
| --- | --- | --- |
| [Get Web API Response Example](actions/get-web-api-response-example.md) | GET | Retrieves a Web API response example from SonarQube. |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook](actions/create-webhook.md) | POST | Creates a webhook in SonarQube. |
| [Delete Webhook](actions/delete-webhook.md) | DELETE | Deletes a webhook from SonarQube. |
| [List Webhooks](actions/list-webhooks.md) | GET | Retrieves webhooks from SonarQube. |
| [Update Webhook](actions/update-webhook.md) | PUT | Updates a webhook in SonarQube. |

### Webhook Delivery

| Action | Method | Description |
| --- | --- | --- |
| [Get Webhook Delivery](actions/get-webhook-delivery.md) | GET | Retrieves a webhook delivery from SonarQube. |
| [List Webhook Deliveries](actions/list-webhook-deliveries.md) | GET | Retrieves webhook deliveries from SonarQube. |

