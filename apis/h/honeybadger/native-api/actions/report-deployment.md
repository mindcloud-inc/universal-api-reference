# Report Deployment with Honeybadger

Reports an application deployment to Honeybadger.

## Endpoint

- **Method:** `POST`
- **Path:** `/deploys`
- **Base URL:** `https://api.honeybadger.io/v1`
- **Official documentation:** [Report Deployment](https://docs.honeybadger.io/api/reporting-deployments/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `deploy.environment` | body | `string` | no | Environment name for the deployment notification. |
| `deploy.revision` | body | `string` | no | VCS revision or tag being deployed. |
| `deploy.repository` | body | `string` | no | HTTPS repository URL for the deployed codebase. |
| `deploy.local_username` | body | `string` | no | User name of the person running the deployment. |
