# AITable.ai: Update Team

Updates an existing team in AITable.ai.

```
PUT https://connect.mindcloud.co/v1/universal/aITableai/latest/actions/update-team
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AITable.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/aITableai/latest/actions/update-team" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "spaceId": "string",
  "unitId": "string",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/aITableai/latest/actions/update-team', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "spaceId": "string",
    "unitId": "string",
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `spaceId` | string | yes | AITable space ID containing the team. |
| `unitId` | string | yes | AITable team unit ID to update. |
| `name` | string | yes | Updated team name. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `sequence` | number | no | Optional team ordering sequence. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "name": "Ava Chen",
      "unitId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `name` | string | Updated team name. |
| `unitId` | string | Updated team unit ID. |

## Native endpoint

Through the native AITable.ai API, this operation is `PUT /fusion/v1/spaces/:spaceId/teams/:unitId` (base URL `https://aitable.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-team.md) for the provider-specific parameters and requirements.

