# CircleCI: Native API Reference

A consolidated summary of CircleCI's API configuration and 94 documented operations, with links to official documentation.

- **Official docs:** https://circleci.com/docs/api/v2/
- **API base URL:** `https://circleci.com/api/v2`

## Authentication

### CircleCI API Token

Use a CircleCI personal API token. CircleCI API v2 requests authenticate with the Circle-Token header.

Send these headers with each API request:

```http
Circle-Token: <apiToken>
```

[Official authentication documentation](https://circleci.com/docs/api/v2/)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON. Response data is read from `data`.

## Endpoints (94 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Approve Pending Approval Job](actions/approve-pending-approval-job.md) | `POST /workflow/:id/approve/:approval_request_id` | [docs](https://circleci.com/docs/api/v2/#tag/Workflow/operation/approvePendingApprovalJobById) |
| [Cancel Job By ID](actions/cancel-job-by-id.md) | `POST /jobs/:job_id/cancel` | [docs](https://circleci.com/docs/api/v2/#tag/Job/operation/cancelJobByJobID) |
| [Cancel Job By Number](actions/cancel-job-by-number.md) | `POST /project/:project_slug/job/:job_number/cancel` | [docs](https://circleci.com/docs/api/v2/#tag/Job/operation/cancelJobByJobNumber) |
| [Cancel Workflow](actions/cancel-workflow.md) | `POST /workflow/:id/cancel` | [docs](https://circleci.com/docs/api/v2/#tag/Workflow/operation/cancelWorkflow) |
| [Continue Pipeline](actions/continue-pipeline.md) | `POST /pipeline/continue` | [docs](https://circleci.com/docs/api/v2/#tag/Pipeline/operation/continuePipeline) |
| [Create Checkout Key](actions/create-checkout-key.md) | `POST /project/:project_slug/checkout-key` | [docs](https://circleci.com/docs/api/v2/#tag/Checkout-Key/operation/createCheckoutKey) |
| [Create Context](actions/create-context.md) | `POST /context` | [docs](https://circleci.com/docs/api/v2/#tag/Context/operation/createContext) |
| [Create Context Restriction](actions/create-context-restriction.md) | `POST /context/:context_id/restrictions` | [docs](https://circleci.com/docs/api/v2/#tag/Context-Restrictions/operation/createContextRestriction) |
| [Create Organization Group](actions/create-organization-group.md) | `POST /organizations/:org_id/groups` | [docs](https://circleci.com/docs/api/v2/#tag/Groups/operation/createOrganizationGroup) |
| [Create Pipeline Definition](actions/create-pipeline-definition.md) | `POST /projects/:project_id/pipeline-definitions` | [docs](https://circleci.com/docs/api/v2/#tag/Pipeline-Definition/operation/createPipelineDefinition) |
| [Create Project](actions/create-project.md) | `POST /organization/:org_slug_or_id/project` | [docs](https://circleci.com/docs/api/v2/#tag/Project/operation/createProject) |
| [Create Project Environment Variable](actions/create-project-environment-variable.md) | `POST /project/:project_slug/envvar` | [docs](https://circleci.com/docs/api/v2/#tag/Environment-Variable/operation/createEnvVar) |
| [Create Schedule](actions/create-schedule.md) | `POST /project/:project_slug/schedule` | [docs](https://circleci.com/docs/api/v2/#tag/Schedule/operation/createSchedule) |
| [Create URL Orb Allow List Entry](actions/create-url-orb-allow-list-entry.md) | `POST /organization/:org_slug_or_id/url-orb-allow-list` | [docs](https://circleci.com/docs/api/v2/#tag/URL-Orb-Allow-List/operation/createURLOrbAllowListEntry) |
| [Create Usage Export Job](actions/create-usage-export-job.md) | `POST /organizations/:org_id/usage_export_job` | [docs](https://circleci.com/docs/api/v2/#tag/Billing/operation/createUsageExport) |
| [Create Webhook](actions/create-webhook.md) | `POST /webhook` | [docs](https://circleci.com/docs/api/v2/#tag/Webhook/operation/createWebhook) |
| [Delete Checkout Key](actions/delete-checkout-key.md) | `DELETE /project/:project_slug/checkout-key/:fingerprint` | [docs](https://circleci.com/docs/api/v2/#tag/Checkout-Key/operation/deleteCheckoutKey) |
| [Delete Context](actions/delete-context.md) | `DELETE /context/:context_id` | [docs](https://circleci.com/docs/api/v2/#tag/Context/operation/deleteContext) |
| [Delete Context Environment Variable](actions/delete-context-environment-variable.md) | `DELETE /context/:context_id/environment-variable/:env_var_name` | [docs](https://circleci.com/docs/api/v2/#tag/Context/operation/deleteEnvironmentVariableFromContext) |
| [Delete Context Restriction](actions/delete-context-restriction.md) | `DELETE /context/:context_id/restrictions/:restriction_id` | [docs](https://circleci.com/docs/api/v2/#tag/Context-Restrictions/operation/deleteContextRestriction) |
| [Delete Organization Group](actions/delete-organization-group.md) | `DELETE /organizations/:org_id/groups/:group_id` | [docs](https://circleci.com/docs/api/v2/#tag/Groups/operation/deleteGroup) |
| [Delete Organization OIDC Claims](actions/delete-organization-oidc-claims.md) | `DELETE /org/:orgID/oidc-custom-claims` | [docs](https://circleci.com/docs/api/v2/#tag/OIDC-Claims/operation/DeleteOrgClaims) |
| [Delete Pipeline Definition](actions/delete-pipeline-definition.md) | `DELETE /projects/:project_id/pipeline-definitions/:pipeline_definition_id` | [docs](https://circleci.com/docs/api/v2/#tag/Pipeline-Definition/operation/deletePipelineDefinition) |
| [Delete Project](actions/delete-project.md) | `DELETE /project/:project_slug` | [docs](https://circleci.com/docs/api/v2/#tag/Project/operation/deleteProjectBySlug) |
| [Delete Project Environment Variable](actions/delete-project-environment-variable.md) | `DELETE /project/:project_slug/envvar/:name` | [docs](https://circleci.com/docs/api/v2/#tag/Environment-Variable/operation/deleteEnvVar) |
| [Delete Project OIDC Claims](actions/delete-project-oidc-claims.md) | `DELETE /org/:orgID/project/:projectID/oidc-custom-claims` | [docs](https://circleci.com/docs/api/v2/#tag/OIDC-Claims/operation/DeleteProjectClaims) |
| [Delete Schedule](actions/delete-schedule.md) | `DELETE /schedule/:schedule_id` | [docs](https://circleci.com/docs/api/v2/#tag/Schedule/operation/deleteScheduleById) |
| [Delete URL Orb Allow List Entry](actions/delete-url-orb-allow-list-entry.md) | `DELETE /organization/:org_slug_or_id/url-orb-allow-list/:allow_list_entry_id` | [docs](https://circleci.com/docs/api/v2/#tag/URL-Orb-Allow-List/operation/removeURLOrbAllowListEntry) |
| [Delete Webhook](actions/delete-webhook.md) | `DELETE /webhook/:webhook_id` | [docs](https://circleci.com/docs/api/v2/#tag/Webhook/operation/deleteWebhook) |
| [Get Checkout Key](actions/get-checkout-key.md) | `GET /project/:project_slug/checkout-key/:fingerprint` | [docs](https://circleci.com/docs/api/v2/#tag/Checkout-Key/operation/getCheckoutKey) |
| [Get Context](actions/get-context.md) | `GET /context/:context_id` | [docs](https://circleci.com/docs/api/v2/#tag/Context/operation/getContext) |
| [Get Current User](actions/get-current-user.md) | `GET /me` | [docs](https://circleci.com/docs/api/v2/#tag/User/operation/getCurrentUser) |
| [Get Deploy Component](actions/get-deploy-component.md) | `GET /deploy/components/:component_id` | [docs](https://circleci.com/docs/api/v2/#tag/Deploy/operation/getComponent) |
| [Get Deploy Environment](actions/get-deploy-environment.md) | `GET /deploy/environments/:environment_id` | [docs](https://circleci.com/docs/api/v2/#tag/Deploy/operation/getEnvironment) |
| [Get Insight Workflow](actions/get-insight-workflow.md) | `GET /insights/:project_slug/workflows/:workflow_name` | [docs](https://circleci.com/docs/api/v2/#tag/Insights/operation/getProjectWorkflowRuns) |
| [Get Insight Workflow Summary](actions/get-insight-workflow-summary.md) | `GET /insights/:project_slug/workflows/:workflow_name/summary` | [docs](https://circleci.com/docs/api/v2/#tag/Insights/operation/getWorkflowSummary) |
| [Get Job](actions/get-job.md) | `GET /jobs/:job_id` | [docs](https://circleci.com/docs/api/v2/#tag/Job/operation/getJob) |
| [Get Job Artifacts](actions/get-job-artifacts.md) | `GET /project/:project_slug/:job_number/artifacts` | [docs](https://circleci.com/docs/api/v2/#tag/Artifacts/operation/getJobArtifacts) |
| [Get Job Tests](actions/get-job-tests.md) | `GET /project/:project_slug/:job_number/tests` | [docs](https://circleci.com/docs/api/v2/#tag/Test-Metadata/operation/getTests) |
| [Get Job Timeseries](actions/get-job-timeseries.md) | `GET /insights/time-series/:project_slug/workflows/:workflow_name/jobs` | [docs](https://circleci.com/docs/api/v2/#tag/Insights/operation/getJobTimeseries) |
| [Get Organization](actions/get-organization.md) | `GET /organization/:org_slug_or_id` | [docs](https://circleci.com/docs/api/v2/#tag/Organization/operation/getOrganization) |
| [Get Organization Group](actions/get-organization-group.md) | `GET /organizations/:org_id/groups/:group_id` | [docs](https://circleci.com/docs/api/v2/#tag/Groups/operation/getGroup) |
| [Get Organization OIDC Claims](actions/get-organization-oidc-claims.md) | `GET /org/:orgID/oidc-custom-claims` | [docs](https://circleci.com/docs/api/v2/#tag/OIDC-Claims/operation/GetOrgClaims) |
| [Get Pipeline](actions/get-pipeline.md) | `GET /pipeline/:pipeline_id` | [docs](https://circleci.com/docs/api/v2/#tag/Pipeline/operation/getPipelineById) |
| [Get Pipeline Config](actions/get-pipeline-config.md) | `GET /pipeline/:pipeline_id/config` | [docs](https://circleci.com/docs/api/v2/#tag/Pipeline/operation/getPipelineConfigById) |
| [Get Pipeline Definition](actions/get-pipeline-definition.md) | `GET /projects/:project_id/pipeline-definitions/:pipeline_definition_id` | [docs](https://circleci.com/docs/api/v2/#tag/Pipeline-Definition/operation/getPipelineDefinition) |
| [Get Pipeline Values](actions/get-pipeline-values.md) | `GET /pipeline/:pipeline_id/values` | [docs](https://circleci.com/docs/api/v2/#tag/Pipeline/operation/getPipelineValuesById) |
| [Get Project By Slug](actions/get-project-by-slug.md) | `GET /project/:project_slug` | [docs](https://circleci.com/docs/api/v2/#tag/Project/operation/getProjectBySlug) |
| [Get Project Environment Variable](actions/get-project-environment-variable.md) | `GET /project/:project_slug/envvar/:name` | [docs](https://circleci.com/docs/api/v2/#tag/Environment-Variable/operation/getEnvVar) |
| [Get Project Job Details](actions/get-project-job-details.md) | `GET /project/:project_slug/job/:job_number` | [docs](https://circleci.com/docs/api/v2/#tag/Job/operation/getJobDetails) |
| [Get Project OIDC Claims](actions/get-project-oidc-claims.md) | `GET /org/:orgID/project/:projectID/oidc-custom-claims` | [docs](https://circleci.com/docs/api/v2/#tag/OIDC-Claims/operation/GetProjectClaims) |
| [Get Project Pipeline By Number](actions/get-project-pipeline-by-number.md) | `GET /project/:project_slug/pipeline/:pipeline_number` | [docs](https://circleci.com/docs/api/v2/#tag/Pipeline/operation/getPipelineByNumber) |
| [Get Project Settings](actions/get-project-settings.md) | `GET /project/:provider/:organization/:project/settings` | [docs](https://circleci.com/docs/api/v2/#tag/Project/operation/getProjectSettings) |
| [Get Project Workflows Page Data](actions/get-project-workflows-page-data.md) | `GET /insights/pages/:project_slug/summary` | [docs](https://circleci.com/docs/api/v2/#tag/Insights/operation/getProjectWorkflowsPageData) |
| [Get Schedule](actions/get-schedule.md) | `GET /schedule/:schedule_id` | [docs](https://circleci.com/docs/api/v2/#tag/Schedule/operation/getScheduleById) |
| [Get Usage Export Job](actions/get-usage-export-job.md) | `GET /organizations/:org_id/usage_export_job/:usage_export_job_id` | [docs](https://circleci.com/docs/api/v2/#tag/Billing/operation/getUsageExport) |
| [Get User](actions/get-user.md) | `GET /user/:id` | [docs](https://circleci.com/docs/api/v2/#tag/User/operation/getUser) |
| [Get Webhook](actions/get-webhook.md) | `GET /webhook/:webhook_id` | [docs](https://circleci.com/docs/api/v2/#tag/Webhook/operation/getWebhookById) |
| [Get Workflow](actions/get-workflow.md) | `GET /workflow/:id` | [docs](https://circleci.com/docs/api/v2/#tag/Workflow/operation/getWorkflowById) |
| [List Checkout Keys](actions/list-checkout-keys.md) | `GET /project/:project_slug/checkout-key` | [docs](https://circleci.com/docs/api/v2/#tag/Checkout-Key/operation/listCheckoutKeys) |
| [List Collaborations](actions/list-collaborations.md) | `GET /me/collaborations` | [docs](https://circleci.com/docs/api/v2/#tag/User/operation/getCollaborations) |
| [List Context Environment Variables](actions/list-context-environment-variables.md) | `GET /context/:context_id/environment-variable` | [docs](https://circleci.com/docs/api/v2/#tag/Context/operation/listEnvironmentVariablesFromContext) |
| [List Context Restrictions](actions/list-context-restrictions.md) | `GET /context/:context_id/restrictions` | [docs](https://circleci.com/docs/api/v2/#tag/Context-Restrictions/operation/getContextRestrictions) |
| [List Contexts](actions/list-contexts.md) | `GET /context` | [docs](https://circleci.com/docs/api/v2/#tag/Context/operation/listContexts) |
| [List Deploy Component Versions](actions/list-deploy-component-versions.md) | `GET /deploy/components/:component_id/versions` | [docs](https://circleci.com/docs/api/v2/#tag/Deploy/operation/listComponentVersions) |
| [List Deploy Components](actions/list-deploy-components.md) | `GET /deploy/components` | [docs](https://circleci.com/docs/api/v2/#tag/Deploy/operation/listComponents) |
| [List Deploy Environments](actions/list-deploy-environments.md) | `GET /deploy/environments` | [docs](https://circleci.com/docs/api/v2/#tag/Deploy/operation/listEnvironments) |
| [List Insight Branches](actions/list-insight-branches.md) | `GET /insights/:project_slug/branches` | [docs](https://circleci.com/docs/api/v2/#tag/Insights/operation/getAllInsightsBranches) |
| [List Insight Workflow Jobs](actions/list-insight-workflow-jobs.md) | `GET /insights/:project_slug/workflows/:workflow_name/jobs` | [docs](https://circleci.com/docs/api/v2/#tag/Insights/operation/getProjectWorkflowJobMetrics) |
| [List Insight Workflow Test Metrics](actions/list-insight-workflow-test-metrics.md) | `GET /insights/:project_slug/workflows/:workflow_name/test-metrics` | [docs](https://circleci.com/docs/api/v2/#tag/Insights/operation/getProjectWorkflowTestMetrics) |
| [List Insight Workflows](actions/list-insight-workflows.md) | `GET /insights/:project_slug/workflows` | [docs](https://circleci.com/docs/api/v2/#tag/Insights/operation/getProjectWorkflowMetrics) |
| [List Organization Groups](actions/list-organization-groups.md) | `GET /organizations/:org_id/groups` | [docs](https://circleci.com/docs/api/v2/#tag/Groups/operation/getOrganizationGroups) |
| [List Pipeline Definition Triggers](actions/list-pipeline-definition-triggers.md) | `GET /projects/:project_id/pipeline-definitions/:pipeline_definition_id/triggers` | [docs](https://circleci.com/docs/api/v2/#tag/Pipeline-Definition/operation/listPipelineDefinitionTriggers) |
| [List Pipeline Definitions](actions/list-pipeline-definitions.md) | `GET /projects/:project_id/pipeline-definitions` | [docs](https://circleci.com/docs/api/v2/#tag/Pipeline-Definition/operation/listPipelineDefinitions) |
| [List Pipeline Workflows](actions/list-pipeline-workflows.md) | `GET /pipeline/:pipeline_id/workflow` | [docs](https://circleci.com/docs/api/v2/#tag/Pipeline/operation/listWorkflowsByPipelineId) |
| [List Pipelines](actions/list-pipelines.md) | `GET /pipeline` | [docs](https://circleci.com/docs/api/v2/#tag/Pipeline/operation/listPipelinesForProject) |
| [List Project Environment Variables](actions/list-project-environment-variables.md) | `GET /project/:project_slug/envvar` | [docs](https://circleci.com/docs/api/v2/#tag/Environment-Variable/operation/listEnvVars) |
| [List Project Pipelines](actions/list-project-pipelines.md) | `GET /project/:project_slug/pipeline` | [docs](https://circleci.com/docs/api/v2/#tag/Pipeline/operation/listPipelinesForProject) |
| [List Project Pipelines Mine](actions/list-project-pipelines-mine.md) | `GET /project/:project_slug/pipeline/mine` | [docs](https://circleci.com/docs/api/v2/#tag/Pipeline/operation/listMyPipelines) |
| [List Project Schedules](actions/list-project-schedules.md) | `GET /project/:project_slug/schedule` | [docs](https://circleci.com/docs/api/v2/#tag/Schedule/operation/listSchedulesForProject) |
| [List URL Orb Allow List Entries](actions/list-url-orb-allow-list-entries.md) | `GET /organization/:org_slug_or_id/url-orb-allow-list` | [docs](https://circleci.com/docs/api/v2/#tag/Organization/operation/listURLOrbAllowListEntries) |
| [List Webhooks](actions/list-webhooks.md) | `GET /webhook` | [docs](https://circleci.com/docs/api/v2/#tag/Webhook/operation/getWebhooks) |
| [List Workflow Jobs](actions/list-workflow-jobs.md) | `GET /workflow/:id/job` | [docs](https://circleci.com/docs/api/v2/#tag/Workflow/operation/listWorkflowJobs) |
| [Patch Organization OIDC Claims](actions/patch-organization-oidc-claims.md) | `PATCH /org/:orgID/oidc-custom-claims` | [docs](https://circleci.com/docs/api/v2/#tag/OIDC-Claims/operation/PatchOrgClaims) |
| [Patch Project OIDC Claims](actions/patch-project-oidc-claims.md) | `PATCH /org/:orgID/project/:projectID/oidc-custom-claims` | [docs](https://circleci.com/docs/api/v2/#tag/OIDC-Claims/operation/PatchProjectClaims) |
| [Patch Project Settings](actions/patch-project-settings.md) | `PATCH /project/:provider/:organization/:project/settings` | [docs](https://circleci.com/docs/api/v2/#tag/Project/operation/patchProjectSettings) |
| [Rerun Workflow](actions/rerun-workflow.md) | `POST /workflow/:id/rerun` | [docs](https://circleci.com/docs/api/v2/#tag/Workflow/operation/rerunWorkflow) |
| [Rollback Project](actions/rollback-project.md) | `POST /projects/:project_id/rollback` | [docs](https://circleci.com/docs/api/v2/#tag/Rollback/operation/rollbackProject) |
| [Trigger Pipeline](actions/trigger-pipeline.md) | `POST /project/:project_slug/pipeline` | [docs](https://circleci.com/docs/api/v2/#tag/Pipeline/operation/triggerPipeline) |
| [Trigger Pipeline Run](actions/trigger-pipeline-run.md) | `POST /project/:provider/:organization/:project/pipeline/run` | [docs](https://circleci.com/docs/api/v2/#tag/Pipeline/operation/triggerPipelineRun) |
| [Update Pipeline Definition](actions/update-pipeline-definition.md) | `PATCH /projects/:project_id/pipeline-definitions/:pipeline_definition_id` | [docs](https://circleci.com/docs/api/v2/#tag/Pipeline-Definition/operation/updatePipelineDefinition) |
| [Update Schedule](actions/update-schedule.md) | `PATCH /schedule/:schedule_id` | [docs](https://circleci.com/docs/api/v2/#tag/Schedule/operation/updateSchedule) |
| [Update Webhook](actions/update-webhook.md) | `PUT /webhook/:webhook_id` | [docs](https://circleci.com/docs/api/v2/#tag/Webhook/operation/updateWebhook) |
| [Upsert Context Environment Variable](actions/upsert-context-environment-variable.md) | `PUT /context/:context_id/environment-variable/:env_var_name` | [docs](https://circleci.com/docs/api/v2/#tag/Context/operation/addEnvironmentVariableToContext) |
