# Freshworks CRM: Update Deal Team

Updates team members for a deal in Freshworks CRM.

```
PUT https://connect.mindcloud.co/v1/universal/freshworksCRM/latest/actions/update-deal-team
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Freshworks CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/freshworksCRM/latest/actions/update-deal-team" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "teamUsers[]": [
    {}
  ],
  "teamUsers[].designationId": 1,
  "teamUsers[].userId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/freshworksCRM/latest/actions/update-deal-team', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "teamUsers[]": [{}],
    "teamUsers[].designationId": 1,
    "teamUsers[].userId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes |  |
| `teamUsers[]` | array<object> | yes |  |
| `teamUsers[].designationId` | number | yes |  |
| `teamUsers[].userId` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "team_users": [
        [
          {}
        ]
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `team_users[]` | array<object> |  |
| `team_users[].created_at` | date |  |
| `team_users[].designation_id` | number |  |
| `team_users[].entity_id` | number |  |
| `team_users[].updated_at` | date |  |
| `team_users[].user_id` | number |  |

## Native endpoint

Through the native Freshworks CRM API, this operation is `POST /api/deals/:id/manage_team_members` (base URL `https://{{credentials.bundleAlias}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-deal-team.md) for the provider-specific parameters and requirements.

