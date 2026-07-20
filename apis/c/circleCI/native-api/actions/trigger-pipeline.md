# Trigger Pipeline with CircleCI

## Endpoint

- **Method:** `POST`
- **Path:** `/project/:project_slug/pipeline`
- **Base URL:** `https://circleci.com/api/v2`
- **Official documentation:** [Trigger Pipeline](https://circleci.com/docs/api/v2/#tag/Pipeline/operation/triggerPipeline)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `branch` | body | `string` | no | Branch to build. |
| `parameters` | body | `string` | no | Pipeline parameters. |
| `project_slug` | path | `string` | no | Project slug in the form vcs/org/repo. |
| `tag` | body | `string` | no | Tag to build. |
