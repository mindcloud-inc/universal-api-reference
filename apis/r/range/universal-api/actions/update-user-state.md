# Range: Update User State

Update a user's state fields with partial state data.

```
PUT https://connect.mindcloud.co/v1/universal/range/latest/actions/update-user-state
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Range `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/range/latest/actions/update-user-state" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/range/latest/actions/update-user-state', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `state` | object | no | Full or partial user state object. |
| `userId` | string | no | The Range user ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accessLevel": 1,
      "asanaIdentifier": "string",
      "billingStatus": "string",
      "calendarLinked": true,
      "clickupUserId": 1,
      "driveLinked": true,
      "dropboxAccountId": "string",
      "githubEnterpriseUserId": 1,
      "githubEnterpriseUsername": "Ava Chen",
      "githubUserId": 1,
      "githubUsername": "Ava Chen",
      "gitlabUserId": 1,
      "hasPassword": true,
      "isVerified": true,
      "jiraAccountId": "string",
      "jiraIdentifier": "string",
      "jiraUsername": "Ava Chen",
      "lastActiveAt": "string",
      "lastInvitedAt": "string",
      "lastInvitedBy": "string",
      "lastReactedAt": "string",
      "lastReadPublishedAt": "string",
      "linearUserId": "string",
      "microsoftUserId": "string",
      "pagerdutyUserId": "string",
      "slackTeamId": "string",
      "slackUserId": "string",
      "spotifyLinked": true,
      "status": 1,
      "termsAcceptedAt": "string",
      "trelloUserId": "string",
      "trelloUsername": "Ava Chen",
      "verifiedEmail": "ava@example.com",
      "zoomUserId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accessLevel` | number |  |
| `asanaIdentifier` | string |  |
| `billingStatus` | string |  |
| `calendarLinked` | boolean |  |
| `clickupUserId` | number |  |
| `driveLinked` | boolean |  |
| `dropboxAccountId` | string |  |
| `githubEnterpriseUserId` | number |  |
| `githubEnterpriseUsername` | string |  |
| `githubUserId` | number |  |
| `githubUsername` | string |  |
| `gitlabUserId` | number |  |
| `hasPassword` | boolean |  |
| `isVerified` | boolean |  |
| `jiraAccountId` | string |  |
| `jiraIdentifier` | string |  |
| `jiraUsername` | string |  |
| `lastActiveAt` | string |  |
| `lastInvitedAt` | string |  |
| `lastInvitedBy` | string |  |
| `lastReactedAt` | string |  |
| `lastReadPublishedAt` | string |  |
| `linearUserId` | string |  |
| `microsoftUserId` | string |  |
| `pagerdutyUserId` | string |  |
| `slackTeamId` | string |  |
| `slackUserId` | string |  |
| `spotifyLinked` | boolean |  |
| `status` | number |  |
| `termsAcceptedAt` | string |  |
| `trelloUserId` | string |  |
| `trelloUsername` | string |  |
| `verifiedEmail` | string |  |
| `zoomUserId` | string |  |

## Native endpoint

Through the native Range API, this operation is `PUT /v1/users/:userId/state` (base URL `https://api.range.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-user-state.md) for the provider-specific parameters and requirements.

