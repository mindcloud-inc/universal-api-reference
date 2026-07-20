# Query with PostHog

Retrieves query results from a PostHog project.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects/:projectId/query/`
- **Base URL:** `https://us.posthog.com/api`
- **Official documentation:** [Query](https://posthog.com/docs/api/query)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `query.query` | body | `string` | no |
| `query` | body | `object` | no |
| `query.kind` | body | `string` | no |
| `async` | body | `string` | no |
| `projectId` | path | `string` | yes |
| `refresh` | body | `string` | no |
