# Statsig: Create Team

Creates a team in Statsig.

```
POST https://connect.mindcloud.co/v1/universal/statsig/latest/actions/create-team-post-console-v1-users-teams
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Statsig `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/statsig/latest/actions/create-team-post-console-v1-users-teams" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "members": "string",
  "admins": "string",
  "defaultGateMetrics": "string",
  "defaultExperimentPrimaryMetrics": "string",
  "defaultExperimentSecondaryMetrics": "string",
  "defaultHoldoutMetrics": "string",
  "changeTeamConfigs": "string",
  "reviewApproval": "string",
  "defaultTargetApplications": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/statsig/latest/actions/create-team-post-console-v1-users-teams', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "members": "string",
    "admins": "string",
    "defaultGateMetrics": "string",
    "defaultExperimentPrimaryMetrics": "string",
    "defaultExperimentSecondaryMetrics": "string",
    "defaultHoldoutMetrics": "string",
    "changeTeamConfigs": "string",
    "reviewApproval": "string",
    "defaultTargetApplications": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Request body field. |
| `description` | string | no | Request body field. |
| `members` | list | yes | Request body field. |
| `admins` | list | yes | Request body field. |
| `defaultGateMetrics` | list | yes | Request body field. |
| `defaultExperimentPrimaryMetrics` | list | yes | Request body field. |
| `defaultExperimentSecondaryMetrics` | list | yes | Request body field. |
| `defaultHoldoutMetrics` | list | yes | Request body field. |
| `changeTeamConfigs` | string | yes | Request body field. |
| `reviewApproval` | string | yes | Request body field. |
| `defaultTargetApplications` | list | yes | Request body field. |
| `defaultHoldoutID` | string | no | Request body field. |
| `requireReviews` | boolean | no | Request body field. |
| `requireGateTemplates` | boolean | no | Request body field. |
| `requireExperimentTemplates` | boolean | no | Request body field. |
| `requireDynamicConfigTemplates` | boolean | no | Request body field. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Statsig response data payload. |
| `message` | string | Statsig response message. |

## Native endpoint

Through the native Statsig API, this operation is `POST /console/v1/users/teams` (base URL `https://statsigapi.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-team-post-console-v1-users-teams.md) for the provider-specific parameters and requirements.

