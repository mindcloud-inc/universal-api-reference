# Create Project with Hasura

Creates a new project in Hasura Cloud.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/graphql`
- **Base URL:** `https://data.pro.hasura.io`
- **Official documentation:** [Create Project](https://hasura.io/docs/2.0/api-reference/cloud-api-reference/#create-a-project)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.cloud` | body | `string` | yes | Hasura Cloud provider identifier, for example aws. |
| `variables.region` | body | `string` | yes | Cloud region for the project, for example us-east-2. |
| `variables.envs[]` | body | `array<object>` | no | Optional environment variables as objects with key and value fields. |
