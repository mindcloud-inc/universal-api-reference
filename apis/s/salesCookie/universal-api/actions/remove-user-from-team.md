# Sales Cookie: Remove User From Team

Removes a user from a team in Sales Cookie.

```
DELETE https://connect.mindcloud.co/v1/universal/salesCookie/latest/actions/remove-user-from-team
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sales Cookie `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/salesCookie/latest/actions/remove-user-from-team?connectionId=$CONNECTION_ID&systemUserId=string&teamId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "systemUserId": "string",
  "teamId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/salesCookie/latest/actions/remove-user-from-team?${params}`, {
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
| `systemUserId` | string | yes | System user ID of the user to remove. |
| `teamId` | string | yes | Team ID to remove the user from. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "systemUserId": "string",
      "teamId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `systemUserId` | string |  |
| `teamId` | string |  |

## Native endpoint

Through the native Sales Cookie API, this operation is `POST /Api/DeleteTeamMember` (base URL `https://salescookie.com/app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-user-from-team.md) for the provider-specific parameters and requirements.

