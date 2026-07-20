# Push by Techulus: Invite User to Team



```
POST https://connect.mindcloud.co/v1/universal/pushByTechulus/latest/actions/invite-user-to-team
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Push by Techulus `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pushByTechulus/latest/actions/invite-user-to-team" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "team": "string",
  "email": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pushByTechulus/latest/actions/invite-user-to-team', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "team": "string",
    "email": "ava@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `team` | string | yes | Team API key supplied from the connection Team credential. |
| `email` | string | yes | Email address of the user to invite to the team. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string | Provider status message for the invite request. |
| `success` | boolean | Whether the team invite request succeeded. |

## Native endpoint

Through the native Push by Techulus API, this operation is `POST /api/management/v1/teams/invite` (base URL `https://push.techulus.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/invite-user-to-team.md) for the provider-specific parameters and requirements.

