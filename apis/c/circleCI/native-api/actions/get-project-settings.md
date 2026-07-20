# Get Project Settings with CircleCI

## Endpoint

- **Method:** `GET`
- **Path:** `/project/:provider/:organization/:project/settings`
- **Base URL:** `https://circleci.com/api/v2`
- **Official documentation:** [Get Project Settings](https://circleci.com/docs/api/v2/#tag/Project/operation/getProjectSettings)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organization` | path | `string` | no | VCS organization name. |
| `project` | path | `string` | no | Repository name. |
| `provider` | path | `string` | no | VCS provider, for example github or bitbucket. |
