# Compare Environments with Diffy

Creates an environment comparison diff in Diffy.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects/:id/compare`
- **Base URL:** `https://app.diffy.website/api`
- **Official documentation:** [Compare Environments](https://app.diffy.website/rest)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `commitSha` | body | `string` | no | Git commit SHA for GitHub checks. |
| `env1` | body | `string` | yes | First environment to compare: prod, stage, dev, or baseline. |
| `env2` | body | `string` | yes | Second environment to compare: prod, stage, dev, or baseline. |
| `id` | path | `number` | yes | Project ID. |
| `name` | body | `string` | no | Custom diff name. |
