# Patch Project Settings with CircleCI

## Endpoint

- **Method:** `PATCH`
- **Path:** `/project/:provider/:organization/:project/settings`
- **Base URL:** `https://circleci.com/api/v2`
- **Official documentation:** [Patch Project Settings](https://circleci.com/docs/api/v2/#tag/Project/operation/patchProjectSettings)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `advanced` | body | `object` | no | Advanced project settings payload. |
| `organization` | path | `string` | no | VCS organization name. |
| `project` | path | `string` | no | Repository name. |
| `provider` | path | `string` | no | VCS provider, for example github or bitbucket. |
