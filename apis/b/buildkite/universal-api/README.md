# <img src="https://images.mindcloud.co/apps/icons/buildkite-icon-square_1775573763254.png" alt="Buildkite logo" width="28" height="28"> Buildkite: Universal API

Buildkite is a CI/CD platform for running pipelines, builds, jobs, artifacts, teams, and organization-level automation workflows.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/buildkite/latest
- **Category:** IT Operations / Developer Tools
- **Actions:** 34
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://buildkite.com
- **Vendor API docs:** https://buildkite.com/docs/apis/rest-api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current Access Token](actions/get-current-access-token.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/buildkite/latest/actions/get-current-access-token?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (34)

### Access Token

| Action | Method | Description |
| --- | --- | --- |
| [Get Current Access Token](actions/get-current-access-token.md) | GET | Retrieves the current access token from Buildkite. |
| [Revoke Current Access Token](actions/revoke-current-access-token.md) | DELETE | Revokes the current access token in Buildkite. |

### Annotation

| Action | Method | Description |
| --- | --- | --- |
| [Create Annotation](actions/create-annotation.md) | POST | Creates a build annotation in Buildkite. |
| [Delete Annotation](actions/delete-annotation.md) | DELETE | Deletes a build annotation from Buildkite. |
| [List Build Annotations](actions/list-build-annotations.md) | GET | Retrieves build annotations from Buildkite. |

### Artifact

| Action | Method | Description |
| --- | --- | --- |
| [Download Artifact](actions/download-artifact.md) | GET | Downloads an artifact from Buildkite. |
| [List Build Artifacts](actions/list-build-artifacts.md) | GET | Retrieves build artifacts from Buildkite. |
| [List Job Artifacts](actions/list-job-artifacts.md) | GET | Retrieves job artifacts from Buildkite. |

### Build

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Build](actions/cancel-build.md) | PUT | Cancels an existing build in Buildkite. |
| [Create Build](actions/create-build.md) | POST | Creates a new build in Buildkite. |
| [Get Build](actions/get-build.md) | GET | Retrieves a build from Buildkite. |
| [List All Builds](actions/list-all-builds.md) | GET | Retrieves all builds from Buildkite. |
| [List Organization Builds](actions/list-organization-builds.md) | GET | Retrieves organization builds from Buildkite. |
| [List Pipeline Builds](actions/list-pipeline-builds.md) | GET | Retrieves pipeline builds from Buildkite. |
| [Rebuild Build](actions/rebuild-build.md) | PUT | Rebuilds an existing build in Buildkite. |

### Job

| Action | Method | Description |
| --- | --- | --- |
| [Delete Job Log](actions/delete-job-log.md) | DELETE | Deletes a job log from Buildkite. |
| [Get Job](actions/get-job.md) | GET | Retrieves a job from Buildkite. |
| [Get Job Log](actions/get-job-log.md) | GET | Retrieves a job log from Buildkite. |
| [Reprioritize Job](actions/reprioritize-job.md) | PUT | Reprioritizes an existing job in Buildkite. |
| [Retry Job](actions/retry-job.md) | PUT | Retries an existing job in Buildkite. |
| [Unblock Job](actions/unblock-job.md) | PUT | Unblocks an existing job in Buildkite. |

### Membership

| Action | Method | Description |
| --- | --- | --- |
| [Get Organization Member](actions/get-organization-member.md) | GET | Retrieves an organization member from Buildkite. |
| [Get Team Member](actions/get-team-member.md) | GET | Retrieves a team member from Buildkite. |
| [List Organization Members](actions/list-organization-members.md) | GET | Retrieves organization members from Buildkite. |
| [List Team Members](actions/list-team-members.md) | GET | Retrieves team members from Buildkite. |

### Organization

| Action | Method | Description |
| --- | --- | --- |
| [Get Organization](actions/get-organization.md) | GET | Retrieves an organization from Buildkite. |
| [List Organizations](actions/list-organizations.md) | GET | Retrieves organizations from Buildkite. |

### Pipeline

| Action | Method | Description |
| --- | --- | --- |
| [Get Pipeline](actions/get-pipeline.md) | GET | Retrieves a pipeline from Buildkite. |
| [Get Team Pipeline](actions/get-team-pipeline.md) | GET | Retrieves a team pipeline from Buildkite. |
| [List Pipelines](actions/list-pipelines.md) | GET | Retrieves pipelines from Buildkite. |
| [List Team Pipelines](actions/list-team-pipelines.md) | GET | Retrieves team pipelines from Buildkite. |

### Team

| Action | Method | Description |
| --- | --- | --- |
| [Get Team](actions/get-team.md) | GET | Retrieves a team from Buildkite. |
| [List Teams](actions/list-teams.md) | GET | Retrieves teams from Buildkite. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | GET | Retrieves the current user from Buildkite. |

