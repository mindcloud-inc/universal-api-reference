# Create Team with Statsig

Creates a team in Statsig.

## Endpoint

- **Method:** `POST`
- **Path:** `/console/v1/users/teams`
- **Base URL:** `https://statsigapi.net`
- **API:** rest
- **Official documentation:** [Create Team](https://docs.statsig.com/api-reference/users/create-team)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Request body field. |
| `description` | body | `string` | no | Request body field. |
| `members` | body | `list` | yes | Request body field. |
| `admins` | body | `list` | yes | Request body field. |
| `defaultGateMetrics` | body | `list` | yes | Request body field. |
| `defaultExperimentPrimaryMetrics` | body | `list` | yes | Request body field. |
| `defaultExperimentSecondaryMetrics` | body | `list` | yes | Request body field. |
| `defaultHoldoutMetrics` | body | `list` | yes | Request body field. |
| `changeTeamConfigs` | body | `string` | yes | Request body field. |
| `reviewApproval` | body | `string` | yes | Request body field. |
| `defaultTargetApplications` | body | `list` | yes | Request body field. |
| `defaultHoldoutID` | body | `string` | no | Request body field. |
| `requireReviews` | body | `boolean` | no | Request body field. |
| `requireGateTemplates` | body | `boolean` | no | Request body field. |
| `requireExperimentTemplates` | body | `boolean` | no | Request body field. |
| `requireDynamicConfigTemplates` | body | `boolean` | no | Request body field. |
