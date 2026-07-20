# Sales Cookie: Add User To Team

Adds a user to a team in Sales Cookie.

```
POST https://connect.mindcloud.co/v1/universal/salesCookie/latest/actions/add-user-to-team
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sales Cookie `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/salesCookie/latest/actions/add-user-to-team" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "systemUserId": "string",
  "teamId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/salesCookie/latest/actions/add-user-to-team', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "systemUserId": "string",
    "teamId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `systemUserId` | string | yes | System user ID of the user to add. |
| `teamId` | string | yes | Team ID to add the user to. |

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

Through the native Sales Cookie API, this operation is `POST /Api/CreateTeamMember` (base URL `https://salescookie.com/app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-user-to-team.md) for the provider-specific parameters and requirements.

