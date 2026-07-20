# Push by Techulus: Delete Invite or Team Member



```
DELETE https://connect.mindcloud.co/v1/universal/pushByTechulus/latest/actions/delete-invite-or-team-member
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Push by Techulus `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/pushByTechulus/latest/actions/delete-invite-or-team-member?connectionId=$CONNECTION_ID&team=string&email=ava%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "team": "string",
  "email": "ava@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pushByTechulus/latest/actions/delete-invite-or-team-member?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `team` | string | yes | Team API key supplied from the connection Team credential. |
| `email` | string | yes | Email address of the invite or team member to remove. |

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
| `message` | string | Provider status message for the removal request. |
| `success` | boolean | Whether the invite or member removal request succeeded. |

## Native endpoint

Through the native Push by Techulus API, this operation is `DELETE /api/management/v1/teams/invite` (base URL `https://push.techulus.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-invite-or-team-member.md) for the provider-specific parameters and requirements.

