# Trigger Pipeline Run with CircleCI

## Endpoint

- **Method:** `POST`
- **Path:** `/project/:provider/:organization/:project/pipeline/run`
- **Base URL:** `https://circleci.com/api/v2`
- **Official documentation:** [Trigger Pipeline Run](https://circleci.com/docs/api/v2/#tag/Pipeline/operation/triggerPipelineRun)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `checkout` | body | `object` | no | Checkout configuration. |
| `config` | body | `object` | no | Config overrides. |
| `definition_id` | body | `string` | no | Pipeline definition identifier to run. |
| `organization` | path | `string` | no | VCS organization name. |
| `parameters` | body | `object` | no | Pipeline parameters. |
| `project` | path | `string` | no | Repository name. |
| `provider` | path | `string` | no | VCS provider, for example github or bitbucket. |
