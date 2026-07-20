# Update team with Statsig

Updates a team in Statsig.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/console/v1/users/teams/{id}`
- **Base URL:** `https://statsigapi.net`
- **API:** rest
- **Official documentation:** [Update team](https://docs.statsig.com/api-reference/users/update-team)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | id |
| `name` | body | `string` | no | Request body field. |
| `description` | body | `string` | no | Request body field. |
| `members` | body | `list` | no | Request body field. |
| `admins` | body | `list` | no | Request body field. |
| `defaultGateMetrics` | body | `list` | no | Request body field. |
| `defaultExperimentPrimaryMetrics` | body | `list` | no | Request body field. |
| `defaultExperimentSecondaryMetrics` | body | `list` | no | Request body field. |
| `defaultHoldoutMetrics` | body | `list` | no | Request body field. |
| `changeTeamConfigs` | body | `string` | no | Request body field. |
| `reviewApproval` | body | `string` | no | Request body field. |
| `defaultTargetApplications` | body | `list` | no | Request body field. |
| `defaultHoldoutID` | body | `string` | no | Request body field. |
| `requireReviews` | body | `boolean` | no | Request body field. |
| `requireGateTemplates` | body | `boolean` | no | Request body field. |
| `requireExperimentTemplates` | body | `boolean` | no | Request body field. |
| `requireDynamicConfigTemplates` | body | `boolean` | no | Request body field. |
