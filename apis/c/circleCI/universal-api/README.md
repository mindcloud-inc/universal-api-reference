# <img src="https://images.mindcloud.co/apps/icons/circleci-icon-512_1775750628600.png" alt="CircleCI logo" width="28" height="28"> CircleCI: Universal API

CircleCI lets teams build, test, and deploy software with pipelines, workflows, jobs, contexts, organization controls, and deployment visibility through the CircleCI API v2.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/circleCI/latest
- **Category:** IT Operations / DevOps
- **Actions:** 94
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://circleci.com
- **Vendor API docs:** https://circleci.com/docs/api/v2/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current User](actions/get-current-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/circleCI/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (94)

### Checkout Key

| Action | Method | Description |
| --- | --- | --- |
| [Create Checkout Key](actions/create-checkout-key.md) | POST |  |
| [Delete Checkout Key](actions/delete-checkout-key.md) | DELETE |  |
| [Get Checkout Key](actions/get-checkout-key.md) | GET |  |
| [List Checkout Keys](actions/list-checkout-keys.md) | GET |  |

### Collaboration

| Action | Method | Description |
| --- | --- | --- |
| [List Collaborations](actions/list-collaborations.md) | GET |  |

### Context

| Action | Method | Description |
| --- | --- | --- |
| [Get Context](actions/get-context.md) | GET |  |
| [List Contexts](actions/list-contexts.md) | GET |  |

### Custom Objects

| Action | Method | Description |
| --- | --- | --- |
| [Create Context](actions/create-context.md) | POST |  |
| [Create Context Restriction](actions/create-context-restriction.md) | POST |  |
| [Create URL Orb Allow List Entry](actions/create-url-orb-allow-list-entry.md) | POST |  |
| [Create Usage Export Job](actions/create-usage-export-job.md) | POST |  |
| [Delete Context](actions/delete-context.md) | DELETE |  |
| [Delete Context Environment Variable](actions/delete-context-environment-variable.md) | DELETE |  |
| [Delete Context Restriction](actions/delete-context-restriction.md) | DELETE |  |
| [Delete Organization OIDC Claims](actions/delete-organization-oidc-claims.md) | DELETE |  |
| [Delete URL Orb Allow List Entry](actions/delete-url-orb-allow-list-entry.md) | DELETE |  |
| [Get Deploy Component](actions/get-deploy-component.md) | GET |  |
| [Get Job Artifacts](actions/get-job-artifacts.md) | GET |  |
| [Get Job Tests](actions/get-job-tests.md) | GET |  |
| [Get Organization OIDC Claims](actions/get-organization-oidc-claims.md) | GET |  |
| [Get Pipeline Config](actions/get-pipeline-config.md) | GET |  |
| [Get Schedule](actions/get-schedule.md) | GET |  |
| [Get Usage Export Job](actions/get-usage-export-job.md) | GET |  |
| [List Context Environment Variables](actions/list-context-environment-variables.md) | GET |  |
| [List Context Restrictions](actions/list-context-restrictions.md) | GET |  |
| [List Deploy Component Versions](actions/list-deploy-component-versions.md) | GET |  |
| [List Deploy Components](actions/list-deploy-components.md) | GET |  |
| [List Project Schedules](actions/list-project-schedules.md) | GET |  |
| [Patch Organization OIDC Claims](actions/patch-organization-oidc-claims.md) | PUT |  |
| [Upsert Context Environment Variable](actions/upsert-context-environment-variable.md) | PUT |  |

### Environments

| Action | Method | Description |
| --- | --- | --- |
| [Get Deploy Environment](actions/get-deploy-environment.md) | GET |  |
| [List Deploy Environments](actions/list-deploy-environments.md) | GET |  |

### Groups

| Action | Method | Description |
| --- | --- | --- |
| [Create Organization Group](actions/create-organization-group.md) | POST |  |
| [Delete Organization Group](actions/delete-organization-group.md) | DELETE |  |
| [Get Organization Group](actions/get-organization-group.md) | GET |  |
| [List Organization Groups](actions/list-organization-groups.md) | GET |  |

### Insight Branch

| Action | Method | Description |
| --- | --- | --- |
| [List Insight Branches](actions/list-insight-branches.md) | GET |  |

### Job

| Action | Method | Description |
| --- | --- | --- |
| [Approve Pending Approval Job](actions/approve-pending-approval-job.md) | PUT |  |
| [Cancel Job By ID](actions/cancel-job-by-id.md) | PUT |  |
| [Cancel Job By Number](actions/cancel-job-by-number.md) | PUT |  |
| [List Insight Workflow Jobs](actions/list-insight-workflow-jobs.md) | GET |  |

### Job Timeseries

| Action | Method | Description |
| --- | --- | --- |
| [Get Job Timeseries](actions/get-job-timeseries.md) | GET |  |

### Jobs

| Action | Method | Description |
| --- | --- | --- |
| [Get Job](actions/get-job.md) | GET |  |
| [Get Project Job Details](actions/get-project-job-details.md) | GET |  |
| [List Workflow Jobs](actions/list-workflow-jobs.md) | GET |  |

### Organization

| Action | Method | Description |
| --- | --- | --- |
| [Get Organization](actions/get-organization.md) | GET |  |

### Pipeline

| Action | Method | Description |
| --- | --- | --- |
| [Continue Pipeline](actions/continue-pipeline.md) | POST |  |
| [List Project Pipelines Mine](actions/list-project-pipelines-mine.md) | GET |  |
| [Trigger Pipeline](actions/trigger-pipeline.md) | POST |  |
| [Trigger Pipeline Run](actions/trigger-pipeline-run.md) | POST |  |

### Pipeline Definition

| Action | Method | Description |
| --- | --- | --- |
| [Create Pipeline Definition](actions/create-pipeline-definition.md) | POST |  |
| [Delete Pipeline Definition](actions/delete-pipeline-definition.md) | DELETE |  |
| [Get Pipeline Definition](actions/get-pipeline-definition.md) | GET |  |
| [List Pipeline Definitions](actions/list-pipeline-definitions.md) | GET |  |
| [Update Pipeline Definition](actions/update-pipeline-definition.md) | PUT |  |

### Pipeline Definition Trigger

| Action | Method | Description |
| --- | --- | --- |
| [List Pipeline Definition Triggers](actions/list-pipeline-definition-triggers.md) | GET |  |

### Pipeline Values

| Action | Method | Description |
| --- | --- | --- |
| [Get Pipeline Values](actions/get-pipeline-values.md) | GET |  |

### Pipelines

| Action | Method | Description |
| --- | --- | --- |
| [Get Pipeline](actions/get-pipeline.md) | GET |  |
| [Get Project Pipeline By Number](actions/get-project-pipeline-by-number.md) | GET |  |
| [List Pipelines](actions/list-pipelines.md) | GET |  |
| [List Project Pipelines](actions/list-project-pipelines.md) | GET |  |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [Create Project](actions/create-project.md) | POST |  |
| [Delete Project](actions/delete-project.md) | DELETE |  |
| [Patch Project Settings](actions/patch-project-settings.md) | PUT |  |
| [Rollback Project](actions/rollback-project.md) | PUT |  |

### Project Environment Variable

| Action | Method | Description |
| --- | --- | --- |
| [Create Project Environment Variable](actions/create-project-environment-variable.md) | POST |  |
| [Delete Project Environment Variable](actions/delete-project-environment-variable.md) | DELETE |  |
| [Get Project Environment Variable](actions/get-project-environment-variable.md) | GET |  |
| [List Project Environment Variables](actions/list-project-environment-variables.md) | GET |  |

### Project Oidc Claims

| Action | Method | Description |
| --- | --- | --- |
| [Delete Project OIDC Claims](actions/delete-project-oidc-claims.md) | DELETE |  |
| [Get Project OIDC Claims](actions/get-project-oidc-claims.md) | GET |  |
| [Patch Project OIDC Claims](actions/patch-project-oidc-claims.md) | PUT |  |

### Project Workflow Summary

| Action | Method | Description |
| --- | --- | --- |
| [Get Project Workflows Page Data](actions/get-project-workflows-page-data.md) | GET |  |

### Projects

| Action | Method | Description |
| --- | --- | --- |
| [Get Project By Slug](actions/get-project-by-slug.md) | GET |  |
| [Get Project Settings](actions/get-project-settings.md) | GET |  |

### Schedule

| Action | Method | Description |
| --- | --- | --- |
| [Create Schedule](actions/create-schedule.md) | POST |  |
| [Delete Schedule](actions/delete-schedule.md) | DELETE |  |
| [Update Schedule](actions/update-schedule.md) | PUT |  |

### Url Orb Allow List Entry

| Action | Method | Description |
| --- | --- | --- |
| [List URL Orb Allow List Entries](actions/list-url-orb-allow-list-entries.md) | GET |  |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | GET |  |
| [Get User](actions/get-user.md) | GET |  |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook](actions/create-webhook.md) | POST |  |
| [Delete Webhook](actions/delete-webhook.md) | DELETE |  |
| [Get Webhook](actions/get-webhook.md) | GET |  |
| [List Webhooks](actions/list-webhooks.md) | GET |  |
| [Update Webhook](actions/update-webhook.md) | PUT |  |

### Workflow

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Workflow](actions/cancel-workflow.md) | PUT |  |
| [Get Insight Workflow](actions/get-insight-workflow.md) | GET |  |
| [Get Insight Workflow Summary](actions/get-insight-workflow-summary.md) | GET |  |
| [List Insight Workflows](actions/list-insight-workflows.md) | GET |  |
| [Rerun Workflow](actions/rerun-workflow.md) | PUT |  |

### Workflow Test Metric

| Action | Method | Description |
| --- | --- | --- |
| [List Insight Workflow Test Metrics](actions/list-insight-workflow-test-metrics.md) | GET |  |

### Workflows

| Action | Method | Description |
| --- | --- | --- |
| [Get Workflow](actions/get-workflow.md) | GET |  |
| [List Pipeline Workflows](actions/list-pipeline-workflows.md) | GET |  |

