# <img src="https://images.mindcloud.co/apps/icons/seqera_1776265471094.png" alt="Seqera logo" width="28" height="28"> Seqera: Universal API

Seqera Platform API for workflow launches, pipeline management, compute environments, datasets, credentials, workspaces, studios, and tokens.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/seqera/latest
- **Category:** IT Operations / Integration & Automation
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://seqera.io
- **Vendor API docs:** https://docs.seqera.io/platform-api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Credentials](actions/list-credentials.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/seqera/latest/actions/list-credentials?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Access Tokens

| Action | Method | Description |
| --- | --- | --- |
| [List Tokens](actions/list-tokens.md) | GET | Retrieves API access tokens from Seqera. |

### Data Sources

| Action | Method | Description |
| --- | --- | --- |
| [List Data Links](actions/list-data-links.md) | GET | Retrieves available data links from Seqera. |

### Datasets

| Action | Method | Description |
| --- | --- | --- |
| [Describe Dataset](actions/describe-dataset.md) | GET | Retrieves dataset metadata from Seqera. |
| [List Datasets](actions/list-datasets.md) | GET | Retrieves datasets from a Seqera workspace. |
| [Upload Dataset Version](actions/upload-dataset-version.md) | POST | Uploads a new dataset version to Seqera. |

### Environments

| Action | Method | Description |
| --- | --- | --- |
| [List Compute Environments](actions/list-compute-environments.md) | GET | Retrieves compute environments from Seqera. |
| [Validate Compute Environment Name](actions/validate-compute-environment-name.md) | GET | Validates a compute environment name in Seqera. |

### Labels

| Action | Method | Description |
| --- | --- | --- |
| [List Labels](actions/list-labels.md) | GET | Retrieves available labels from Seqera. |

### Organizations

| Action | Method | Description |
| --- | --- | --- |
| [List Organizations](actions/list-organizations.md) | GET | Retrieves available organizations from Seqera. |

### Pipelines

| Action | Method | Description |
| --- | --- | --- |
| [Describe Pipeline Launch](actions/describe-pipeline-launch.md) | GET | Retrieves pipeline launch details from Seqera. |
| [Describe Remote Pipeline Repository](actions/describe-pipeline-repository.md) | GET | Retrieves remote pipeline repository details from Seqera. |
| [Describe Pipeline Schema](actions/describe-pipeline-schema.md) | GET | Retrieves a pipeline schema from Seqera. |
| [List Pipeline Versions](actions/list-pipeline-versions.md) | GET | Retrieves pipeline versions from Seqera. |
| [List Pipelines](actions/list-pipelines.md) | GET | Retrieves available pipelines from Seqera. |
| [Validate Pipeline Name](actions/validate-pipeline-name.md) | GET | Validates a pipeline name in Seqera. |

### Roles

| Action | Method | Description |
| --- | --- | --- |
| [List Roles](actions/list-roles.md) | GET | Retrieves available roles from Seqera. |

### Secrets

| Action | Method | Description |
| --- | --- | --- |
| [Get Encrypted Credentials](actions/get-encrypted-credentials.md) | GET | Retrieves encrypted credential keys from Seqera. |
| [List Credentials](actions/list-credentials.md) | GET | Retrieves available credentials from Seqera. |
| [List SSH Keys](actions/list-ssh-keys.md) | GET | Retrieves SSH public keys from Seqera. |
| [Validate Credential Name](actions/validate-credential-name.md) | GET | Validates a credential name in Seqera. |

### Services

| Action | Method | Description |
| --- | --- | --- |
| [List Studios](actions/list-studios.md) | GET | Retrieves available Studios from Seqera. |

### Workflow Runs

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Run](actions/cancel-run.md) | PUT | Cancels a workflow run in Seqera. |
| [Describe Run](actions/describe-run.md) | GET | Retrieves workflow run details from Seqera. |
| [List Runs](actions/list-runs.md) | GET | Retrieves workflow runs from Seqera. |
| [Retrieve Run Status](actions/retrieve-run-status.md) | GET | Retrieves a workflow run status from Seqera. |

### Workspaces

| Action | Method | Description |
| --- | --- | --- |
| [Create Workspace Participant](actions/create-workspace-participant.md) | POST | Adds a new workspace participant in Seqera. |
| [Describe Workspace](actions/describe-workspace.md) | GET | Retrieves workspace details from Seqera. |
| [List Organization Workspaces](actions/list-organization-workspaces.md) | GET | Retrieves organization workspaces from Seqera. |
| [List Workspace Participants](actions/list-workspace-participants.md) | GET | Retrieves workspace participants from Seqera. |
| [Update Workspace Participant Role](actions/update-workspace-participant-role.md) | PUT | Updates a workspace participant role in Seqera. |

