# AITable.ai: Create Team

Creates a new team in AITable.ai.

```
POST https://connect.mindcloud.co/v1/universal/aITableai/latest/actions/create-team
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AITable.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/aITableai/latest/actions/create-team" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "spaceId": "string",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/aITableai/latest/actions/create-team', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "spaceId": "string",
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `spaceId` | string | yes | AITable space ID where the team will be created. |
| `name` | string | yes | Name of the team to create. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `parentUnitId` | string | no | Optional parent team unit ID. |

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
| `name` | string | Created team name. |
| `unitId` | string | Created team unit ID. |

## Native endpoint

Through the native AITable.ai API, this operation is `POST /fusion/v1/spaces/:spaceId/teams` (base URL `https://aitable.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-team.md) for the provider-specific parameters and requirements.

