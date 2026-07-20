# Stormboard: Create Storm

Creates a Storm in Stormboard.

```
POST https://connect.mindcloud.co/v1/universal/stormboard/latest/actions/create-storm
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stormboard `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/stormboard/latest/actions/create-storm" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "plan": "string",
  "title": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/stormboard/latest/actions/create-storm', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "plan": "string",
    "title": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `avatars` | string | no | Set to 1 to show user avatars in real time, or 0 to hide them. |
| `description` | string | no | Storm description or goals. |
| `ideaCreator` | string | no | Set to 1 to show the idea creator avatar on ideas, or 0 to hide it. |
| `plan` | string | yes | Plan type for the new storm: personal, student, educator, or team. |
| `teamId` | number | no | Team ID to use when plan is team. |
| `templateId` | number | no | Template ID for the storm. |
| `title` | string | yes | Title of the new storm. |
| `votesPerUser` | number | no | Number of votes each user gets. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "goals": "string",
      "id": 1,
      "ideacreator": 1,
      "key": "string",
      "message": "string",
      "status": 1,
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `goals` | string |  |
| `id` | number |  |
| `ideacreator` | number |  |
| `key` | string |  |
| `message` | string |  |
| `status` | number |  |
| `title` | string |  |

## Native endpoint

Through the native Stormboard API, this operation is `POST /storms` (base URL `https://api.stormboard.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-storm.md) for the provider-specific parameters and requirements.

