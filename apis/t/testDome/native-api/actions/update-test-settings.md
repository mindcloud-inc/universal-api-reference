# Update Test Settings with TestDome

Updates test settings in TestDome.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/tests/:testId/settings`
- **Base URL:** `https://api.staging.testdome.com/v3`
- **Official documentation:** [Update Test Settings](https://api.testdome.com/openapi-ui/index/index.html?urls.primaryName=v3%20Docs)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `databaseOptions` | body | `list<string>` | no |
| `description` | body | `string` | no |
| `id` | path | `number` | yes |
| `integrationDeadlineInDays` | body | `number` | no |
| `integrationProctoring` | body | `boolean` | no |
| `isAiForbidden` | body | `boolean` | no |
| `name` | body | `string` | yes |
| `notifyTo` | body | `list<string>` | no |
| `showFinalScoreToCandidate` | body | `boolean` | yes |
| `timingPolicy` | body | `string` | yes |
