# SonarQube: Native API Reference

A consolidated summary of SonarQube's API configuration and 128 documented operations, with links to official documentation.

- **Official docs:** https://docs.sonarsource.com/sonarqube/latest/extension-guide/web-api/
- **API base URL:** `https://sonarcloud.io`

## Authentication

### API Key

SonarQube/SonarCloud user token sent as a Bearer token in the Authorization header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.sonarsource.com/sonarqube/latest/extension-guide/web-api/)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (128 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Activate Quality Profile Rule](actions/activate-quality-profile-rule.md) | `POST /api/qualityprofiles/activate_rule` | [docs](https://sonarcloud.io/web_api/api/qualityprofiles/activate_rule) |
| [Activate Quality Profile Rules](actions/activate-quality-profile-rules.md) | `POST /api/qualityprofiles/activate_rules` | [docs](https://sonarcloud.io/web_api/api/qualityprofiles/activate_rules) |
| [Add Favorite](actions/add-favorite.md) | `POST /api/favorites/add` | [docs](https://sonarcloud.io/web_api/api/favorites/add) |
| [Add Group Permission](actions/add-group-permission.md) | `POST /api/permissions/add_group` | [docs](https://sonarcloud.io/web_api/api/permissions/add_group) |
| [Add Group To Permission Template](actions/add-group-to-permission-template.md) | `POST /api/permissions/add_group_to_template` | [docs](https://sonarcloud.io/web_api/api/permissions/add_group_to_template) |
| [Add Issue Comment](actions/add-issue-comment.md) | `POST /api/issues/add_comment` | [docs](https://sonarcloud.io/web_api/api/issues/add_comment) |
| [Add Notification](actions/add-notification.md) | `POST /api/notifications/add` | [docs](https://sonarcloud.io/web_api/api/notifications/add) |
| [Add Project Creator To Permission Template](actions/add-project-creator-to-permission-template.md) | `POST /api/permissions/add_project_creator_to_template` | [docs](https://sonarcloud.io/web_api/api/permissions/add_project_creator_to_template) |
| [Add Project To Quality Profile](actions/add-project-to-quality-profile.md) | `POST /api/qualityprofiles/add_project` | [docs](https://sonarcloud.io/web_api/api/qualityprofiles/add_project) |
| [Add User Permission](actions/add-user-permission.md) | `POST /api/permissions/add_user` | [docs](https://sonarcloud.io/web_api/api/permissions/add_user) |
| [Add User To Group](actions/add-user-to-group.md) | `POST /api/user_groups/add_user` | [docs](https://sonarcloud.io/web_api/api/user_groups/add_user) |
| [Add User To Permission Template](actions/add-user-to-permission-template.md) | `POST /api/permissions/add_user_to_template` | [docs](https://sonarcloud.io/web_api/api/permissions/add_user_to_template) |
| [Apply Permission Template](actions/apply-permission-template.md) | `POST /api/permissions/apply_template` | [docs](https://sonarcloud.io/web_api/api/permissions/apply_template) |
| [Assign Issue](actions/assign-issue.md) | `POST /api/issues/assign` | [docs](https://sonarcloud.io/web_api/api/issues/assign) |
| [Backup Quality Profile](actions/backup-quality-profile.md) | `GET /api/qualityprofiles/backup` | [docs](https://sonarcloud.io/web_api/api/qualityprofiles/backup) |
| [Bulk Apply Permission Template](actions/bulk-apply-permission-template.md) | `POST /api/permissions/bulk_apply_template` | [docs](https://sonarcloud.io/web_api/api/permissions/bulk_apply_template) |
| [Bulk Change Issues](actions/bulk-change-issues.md) | `POST /api/issues/bulk_change` | [docs](https://sonarcloud.io/web_api/api/issues/bulk_change) |
| [Bulk Delete Projects](actions/bulk-delete-projects.md) | `POST /api/projects/bulk_delete` | [docs](https://sonarcloud.io/web_api/api/projects/bulk_delete) |
| [Change Quality Profile Parent](actions/change-quality-profile-parent.md) | `POST /api/qualityprofiles/change_parent` | [docs](https://sonarcloud.io/web_api/api/qualityprofiles/change_parent) |
| [Change Security Hotspot Status](actions/change-security-hotspot-status.md) | `POST /api/hotspots/change_status` | [docs](https://sonarcloud.io/web_api/api/hotspots/change_status) |
| [Copy Quality Profile](actions/copy-quality-profile.md) | `POST /api/qualityprofiles/copy` | [docs](https://sonarcloud.io/web_api/api/qualityprofiles/copy) |
| [Create Permission Template](actions/create-permission-template.md) | `POST /api/permissions/create_template` | [docs](https://sonarcloud.io/web_api/api/permissions/create_template) |
| [Create Project](actions/create-project.md) | `POST /api/projects/create` | [docs](https://sonarcloud.io/web_api/api/projects/create) |
| [Create Project Analysis Event](actions/create-project-analysis-event.md) | `POST /api/project_analyses/create_event` | [docs](https://sonarcloud.io/web_api/api/project_analyses/create_event) |
| [Create Project Link](actions/create-project-link.md) | `POST /api/project_links/create` | [docs](https://sonarcloud.io/web_api/api/project_links/create) |
| [Create Quality Profile](actions/create-quality-profile.md) | `POST /api/qualityprofiles/create` | [docs](https://sonarcloud.io/web_api/api/qualityprofiles/create) |
| [Create User Group](actions/create-user-group.md) | `POST /api/user_groups/create` | [docs](https://sonarcloud.io/web_api/api/user_groups/create) |
| [Create Webhook](actions/create-webhook.md) | `POST /api/webhooks/create` | [docs](https://sonarcloud.io/web_api/api/webhooks/create) |
| [Deactivate Quality Profile Rule](actions/deactivate-quality-profile-rule.md) | `POST /api/qualityprofiles/deactivate_rule` | [docs](https://sonarcloud.io/web_api/api/qualityprofiles/deactivate_rule) |
| [Deactivate Quality Profile Rules](actions/deactivate-quality-profile-rules.md) | `POST /api/qualityprofiles/deactivate_rules` | [docs](https://sonarcloud.io/web_api/api/qualityprofiles/deactivate_rules) |
| [Delete Issue Comment](actions/delete-issue-comment.md) | `POST /api/issues/delete_comment` | [docs](https://sonarcloud.io/web_api/api/issues/delete_comment) |
| [Delete Permission Template](actions/delete-permission-template.md) | `POST /api/permissions/delete_template` | [docs](https://sonarcloud.io/web_api/api/permissions/delete_template) |
| [Delete Project](actions/delete-project.md) | `POST /api/projects/delete` | [docs](https://sonarcloud.io/web_api/api/projects/delete) |
| [Delete Project Analysis](actions/delete-project-analysis.md) | `POST /api/project_analyses/delete` | [docs](https://sonarcloud.io/web_api/api/project_analyses/delete) |
| [Delete Project Analysis Event](actions/delete-project-analysis-event.md) | `POST /api/project_analyses/delete_event` | [docs](https://sonarcloud.io/web_api/api/project_analyses/delete_event) |
| [Delete Project Branch](actions/delete-project-branch.md) | `POST /api/project_branches/delete` | [docs](https://sonarcloud.io/web_api/api/project_branches/delete) |
| [Delete Project Link](actions/delete-project-link.md) | `POST /api/project_links/delete` | [docs](https://sonarcloud.io/web_api/api/project_links/delete) |
| [Delete Project Pull Request](actions/delete-project-pull-request.md) | `POST /api/project_pull_requests/delete` | [docs](https://sonarcloud.io/web_api/api/project_pull_requests/delete) |
| [Delete Quality Profile](actions/delete-quality-profile.md) | `POST /api/qualityprofiles/delete` | [docs](https://sonarcloud.io/web_api/api/qualityprofiles/delete) |
| [Delete User Group](actions/delete-user-group.md) | `POST /api/user_groups/delete` | [docs](https://sonarcloud.io/web_api/api/user_groups/delete) |
| [Delete Webhook](actions/delete-webhook.md) | `POST /api/webhooks/delete` | [docs](https://sonarcloud.io/web_api/api/webhooks/delete) |
| [Edit Issue Comment](actions/edit-issue-comment.md) | `POST /api/issues/edit_comment` | [docs](https://sonarcloud.io/web_api/api/issues/edit_comment) |
| [Generate User Token](actions/generate-user-token.md) | `POST /api/user_tokens/generate` | [docs](https://sonarcloud.io/web_api/api/user_tokens/generate) |
| [Get AI Code Assurance Badge](actions/get-ai-code-assurance-badge.md) | `GET /api/project_badges/ai_code_assurance` | [docs](https://sonarcloud.io/web_api/api/project_badges/ai_code_assurance) |
| [Get Component Measures](actions/get-component-measures.md) | `GET /api/measures/component` | [docs](https://sonarcloud.io/web_api/api/measures/component) |
| [Get Compute Engine Activity Status](actions/get-compute-engine-activity-status.md) | `GET /api/ce/activity_status` | [docs](https://sonarcloud.io/web_api/api/ce/activity_status) |
| [Get Compute Engine Component](actions/get-compute-engine-component.md) | `GET /api/ce/component` | [docs](https://sonarcloud.io/web_api/api/ce/component) |
| [Get Compute Engine Task](actions/get-compute-engine-task.md) | `GET /api/ce/task` | [docs](https://sonarcloud.io/web_api/api/ce/task) |
| [Get Issue Changelog](actions/get-issue-changelog.md) | `GET /api/issues/changelog` | [docs](https://sonarcloud.io/web_api/api/issues/changelog) |
| [Get Project Measure Badge](actions/get-project-measure-badge.md) | `GET /api/project_badges/measure` | [docs](https://sonarcloud.io/web_api/api/project_badges/measure) |
| [Get Project Quality Gate Badge](actions/get-project-quality-gate-badge.md) | `GET /api/project_badges/quality_gate` | [docs](https://sonarcloud.io/web_api/api/project_badges/quality_gate) |
| [Get Quality Profile Changelog](actions/get-quality-profile-changelog.md) | `GET /api/qualityprofiles/changelog` | [docs](https://sonarcloud.io/web_api/api/qualityprofiles/changelog) |
| [Get Quality Profile Inheritance](actions/get-quality-profile-inheritance.md) | `GET /api/qualityprofiles/inheritance` | [docs](https://sonarcloud.io/web_api/api/qualityprofiles/inheritance) |
| [Get Raw Source](actions/get-raw-source.md) | `GET /api/sources/raw` | [docs](https://sonarcloud.io/web_api/api/sources/raw) |
| [Get Setting Values](actions/get-setting-values.md) | `GET /api/settings/values` | [docs](https://sonarcloud.io/web_api/api/settings/values) |
| [Get Source SCM](actions/get-source-scm.md) | `GET /api/sources/scm` | [docs](https://sonarcloud.io/web_api/api/sources/scm) |
| [Get Web API Response Example](actions/get-web-api-response-example.md) | `GET /api/webservices/response_example` | [docs](https://sonarcloud.io/web_api/api/webservices/response_example) |
| [Get Webhook Delivery](actions/get-webhook-delivery.md) | `GET /api/webhooks/delivery` | [docs](https://sonarcloud.io/web_api/api/webhooks/delivery) |
| [List Component Measures](actions/list-component-measures.md) | `GET /api/measures/component_tree` | [docs](https://sonarcloud.io/web_api/api/measures/component_tree) |
| [List Component Tree](actions/list-component-tree.md) | `GET /api/components/tree` | [docs](https://sonarcloud.io/web_api/api/components/tree) |
| [List Issue Authors](actions/list-issue-authors.md) | `GET /api/issues/authors` | [docs](https://sonarcloud.io/web_api/api/issues/authors) |
| [List Issue Tags](actions/list-issue-tags.md) | `GET /api/issues/tags` | [docs](https://sonarcloud.io/web_api/api/issues/tags) |
| [List Languages](actions/list-languages.md) | `GET /api/languages/list` | [docs](https://sonarcloud.io/web_api/api/languages/list) |
| [List Metric Types](actions/list-metric-types.md) | `GET /api/metrics/types` | [docs](https://sonarcloud.io/web_api/api/metrics/types) |
| [List Notifications](actions/list-notifications.md) | `GET /api/notifications/list` | [docs](https://sonarcloud.io/web_api/api/notifications/list) |
| [List Project Branches](actions/list-project-branches.md) | `GET /api/project_branches/list` | [docs](https://sonarcloud.io/web_api/api/project_branches/list) |
| [List Project Pull Requests](actions/list-project-pull-requests.md) | `GET /api/project_pull_requests/list` | [docs](https://sonarcloud.io/web_api/api/project_pull_requests/list) |
| [List Quality Profile Projects](actions/list-quality-profile-projects.md) | `GET /api/qualityprofiles/projects` | [docs](https://sonarcloud.io/web_api/api/qualityprofiles/projects) |
| [List Rule Repositories](actions/list-rule-repositories.md) | `GET /api/rules/repositories` | [docs](https://sonarcloud.io/web_api/api/rules/repositories) |
| [List Rule Tags](actions/list-rule-tags.md) | `GET /api/rules/tags` | [docs](https://sonarcloud.io/web_api/api/rules/tags) |
| [List Setting Definitions](actions/list-setting-definitions.md) | `GET /api/settings/list_definitions` | [docs](https://sonarcloud.io/web_api/api/settings/list_definitions) |
| [List User Group Members](actions/list-user-group-members.md) | `GET /api/user_groups/users` | [docs](https://sonarcloud.io/web_api/api/user_groups/users) |
| [List User Groups For User](actions/list-user-groups-for-user.md) | `GET /api/users/groups` | [docs](https://sonarcloud.io/web_api/api/users/groups) |
| [List User Tokens](actions/list-user-tokens.md) | `GET /api/user_tokens/search` | [docs](https://sonarcloud.io/web_api/api/user_tokens/search) |
| [List Web API Endpoints](actions/list-web-api-endpoints.md) | `GET /api/webservices/list` | [docs](https://sonarcloud.io/web_api/api/webservices/list) |
| [List Webhook Deliveries](actions/list-webhook-deliveries.md) | `GET /api/webhooks/deliveries` | [docs](https://sonarcloud.io/web_api/api/webhooks/deliveries) |
| [List Webhooks](actions/list-webhooks.md) | `GET /api/webhooks/list` | [docs](https://sonarcloud.io/web_api/api/webhooks/list) |
| [Logout](actions/logout.md) | `POST /api/authentication/logout` | [docs](https://sonarcloud.io/web_api/api/authentication/logout) |
| [Remove Favorite](actions/remove-favorite.md) | `POST /api/favorites/remove` | [docs](https://sonarcloud.io/web_api/api/favorites/remove) |
| [Remove Group From Permission Template](actions/remove-group-from-permission-template.md) | `POST /api/permissions/remove_group_from_template` | [docs](https://sonarcloud.io/web_api/api/permissions/remove_group_from_template) |
| [Remove Group Permission](actions/remove-group-permission.md) | `POST /api/permissions/remove_group` | [docs](https://sonarcloud.io/web_api/api/permissions/remove_group) |
| [Remove Notification](actions/remove-notification.md) | `POST /api/notifications/remove` | [docs](https://sonarcloud.io/web_api/api/notifications/remove) |
| [Remove Project Creator From Permission Template](actions/remove-project-creator-from-permission-template.md) | `POST /api/permissions/remove_project_creator_from_template` | [docs](https://sonarcloud.io/web_api/api/permissions/remove_project_creator_from_template) |
| [Remove Project From Quality Profile](actions/remove-project-from-quality-profile.md) | `POST /api/qualityprofiles/remove_project` | [docs](https://sonarcloud.io/web_api/api/qualityprofiles/remove_project) |
| [Remove User From Group](actions/remove-user-from-group.md) | `POST /api/user_groups/remove_user` | [docs](https://sonarcloud.io/web_api/api/user_groups/remove_user) |
| [Remove User From Permission Template](actions/remove-user-from-permission-template.md) | `POST /api/permissions/remove_user_from_template` | [docs](https://sonarcloud.io/web_api/api/permissions/remove_user_from_template) |
| [Remove User Permission](actions/remove-user-permission.md) | `POST /api/permissions/remove_user` | [docs](https://sonarcloud.io/web_api/api/permissions/remove_user) |
| [Rename Project Branch](actions/rename-project-branch.md) | `POST /api/project_branches/rename` | [docs](https://sonarcloud.io/web_api/api/project_branches/rename) |
| [Rename Quality Profile](actions/rename-quality-profile.md) | `POST /api/qualityprofiles/rename` | [docs](https://sonarcloud.io/web_api/api/qualityprofiles/rename) |
| [Reset Settings](actions/reset-settings.md) | `POST /api/settings/reset` | [docs](https://sonarcloud.io/web_api/api/settings/reset) |
| [Restore Quality Profile](actions/restore-quality-profile.md) | `POST /api/qualityprofiles/restore` | [docs](https://sonarcloud.io/web_api/api/qualityprofiles/restore) |
| [Revoke User Token](actions/revoke-user-token.md) | `POST /api/user_tokens/revoke` | [docs](https://sonarcloud.io/web_api/api/user_tokens/revoke) |
| [Search Components](actions/search-components.md) | `GET /api/components/search` | [docs](https://sonarcloud.io/web_api/api/components/search) |
| [Search Compute Engine Tasks](actions/search-compute-engine-tasks.md) | `GET /api/ce/activity` | [docs](https://sonarcloud.io/web_api/api/ce/activity) |
| [Search Favorites](actions/search-favorites.md) | `GET /api/favorites/search` | [docs](https://sonarcloud.io/web_api/api/favorites/search) |
| [Search Issues](actions/search-issues.md) | `GET /api/issues/search` | [docs](https://sonarcloud.io/web_api/api/issues/search) |
| [Search Measure History](actions/search-measure-history.md) | `GET /api/measures/search_history` | [docs](https://sonarcloud.io/web_api/api/measures/search_history) |
| [Search Metrics](actions/search-metrics.md) | `GET /api/metrics/search` | [docs](https://sonarcloud.io/web_api/api/metrics/search) |
| [Search Permission Templates](actions/search-permission-templates.md) | `GET /api/permissions/search_templates` | [docs](https://sonarcloud.io/web_api/api/permissions/search_templates) |
| [Search Project Analyses](actions/search-project-analyses.md) | `GET /api/project_analyses/search` | [docs](https://sonarcloud.io/web_api/api/project_analyses/search) |
| [Search Project Links](actions/search-project-links.md) | `GET /api/project_links/search` | [docs](https://sonarcloud.io/web_api/api/project_links/search) |
| [Search Project Tags](actions/search-project-tags.md) | `GET /api/project_tags/search` | [docs](https://sonarcloud.io/web_api/api/project_tags/search) |
| [Search Projects](actions/search-projects.md) | `GET /api/projects/search` | [docs](https://sonarcloud.io/web_api/api/projects/search) |
| [Search Quality Profiles](actions/search-quality-profiles.md) | `GET /api/qualityprofiles/search` | [docs](https://sonarcloud.io/web_api/api/qualityprofiles/search) |
| [Search Rules](actions/search-rules.md) | `GET /api/rules/search` | [docs](https://sonarcloud.io/web_api/api/rules/search) |
| [Search Security Hotspots](actions/search-security-hotspots.md) | `GET /api/hotspots/search` | [docs](https://sonarcloud.io/web_api/api/hotspots/search) |
| [Search User Groups](actions/search-user-groups.md) | `GET /api/user_groups/search` | [docs](https://sonarcloud.io/web_api/api/user_groups/search) |
| [Set Default Permission Template](actions/set-default-permission-template.md) | `POST /api/permissions/set_default_template` | [docs](https://sonarcloud.io/web_api/api/permissions/set_default_template) |
| [Set Default Quality Profile](actions/set-default-quality-profile.md) | `POST /api/qualityprofiles/set_default` | [docs](https://sonarcloud.io/web_api/api/qualityprofiles/set_default) |
| [Set Issue Tags](actions/set-issue-tags.md) | `POST /api/issues/set_tags` | [docs](https://sonarcloud.io/web_api/api/issues/set_tags) |
| [Set Project Analysis Baseline](actions/set-project-analysis-baseline.md) | `POST /api/project_analyses/set_baseline` | [docs](https://sonarcloud.io/web_api/api/project_analyses/set_baseline) |
| [Set Project Tags](actions/set-project-tags.md) | `POST /api/project_tags/set` | [docs](https://sonarcloud.io/web_api/api/project_tags/set) |
| [Set Setting](actions/set-setting.md) | `POST /api/settings/set` | [docs](https://sonarcloud.io/web_api/api/settings/set) |
| [Show Component](actions/show-component.md) | `GET /api/components/show` | [docs](https://sonarcloud.io/web_api/api/components/show) |
| [Show Duplications](actions/show-duplications.md) | `GET /api/duplications/show` | [docs](https://sonarcloud.io/web_api/api/duplications/show) |
| [Show Rule](actions/show-rule.md) | `GET /api/rules/show` | [docs](https://sonarcloud.io/web_api/api/rules/show) |
| [Show Security Hotspot](actions/show-security-hotspot.md) | `GET /api/hotspots/show` | [docs](https://sonarcloud.io/web_api/api/hotspots/show) |
| [Show Source](actions/show-source.md) | `GET /api/sources/show` | [docs](https://sonarcloud.io/web_api/api/sources/show) |
| [Transition Issue](actions/transition-issue.md) | `POST /api/issues/do_transition` | [docs](https://sonarcloud.io/web_api/api/issues/do_transition) |
| [Unset Project Analysis Baseline](actions/unset-project-analysis-baseline.md) | `POST /api/project_analyses/unset_baseline` | [docs](https://sonarcloud.io/web_api/api/project_analyses/unset_baseline) |
| [Update Permission Template](actions/update-permission-template.md) | `POST /api/permissions/update_template` | [docs](https://sonarcloud.io/web_api/api/permissions/update_template) |
| [Update Project Analysis Event](actions/update-project-analysis-event.md) | `POST /api/project_analyses/update_event` | [docs](https://sonarcloud.io/web_api/api/project_analyses/update_event) |
| [Update Project Key](actions/update-project-key.md) | `POST /api/projects/update_key` | [docs](https://sonarcloud.io/web_api/api/projects/update_key) |
| [Update Project Visibility](actions/update-project-visibility.md) | `POST /api/projects/update_visibility` | [docs](https://sonarcloud.io/web_api/api/projects/update_visibility) |
| [Update Rule](actions/update-rule.md) | `POST /api/rules/update` | [docs](https://sonarcloud.io/web_api/api/rules/update) |
| [Update User Group](actions/update-user-group.md) | `POST /api/user_groups/update` | [docs](https://sonarcloud.io/web_api/api/user_groups/update) |
| [Update Webhook](actions/update-webhook.md) | `POST /api/webhooks/update` | [docs](https://sonarcloud.io/web_api/api/webhooks/update) |
| [Validate Authentication](actions/validate-authentication.md) | `GET /api/authentication/validate` | [docs](https://sonarcloud.io/web_api/api/authentication/validate) |
