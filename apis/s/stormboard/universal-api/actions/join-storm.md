# Stormboard: Join Storm

Joins a Storm in Stormboard.

```
POST https://connect.mindcloud.co/v1/universal/stormboard/latest/actions/join-storm
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stormboard `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/stormboard/latest/actions/join-storm" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "stormId": 1,
  "stormKey": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/stormboard/latest/actions/join-storm', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "stormId": 1,
    "stormKey": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `stormId` | number | yes | Storm ID from the Stormboard share dialog. |
| `stormKey` | string | yes | Private storm key from the Stormboard share dialog. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "status": 1,
      "storm": {
        "admin": 1,
        "avatars": 1,
        "chatlocked": 1,
        "goals": "string",
        "id": 1,
        "ideacreator": 1,
        "key": "string",
        "lastactivity": "string",
        "plan": "string",
        "status": "string",
        "thumbnail": "string",
        "title": "string",
        "votesperadmin": 1,
        "votesperuser": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |
| `status` | number |  |
| `storm` | object |  |
| `storm.admin` | number |  |
| `storm.avatars` | number |  |
| `storm.chatlocked` | number |  |
| `storm.goals` | string |  |
| `storm.id` | number |  |
| `storm.ideacreator` | number |  |
| `storm.key` | string |  |
| `storm.lastactivity` | string |  |
| `storm.plan` | string |  |
| `storm.status` | string |  |
| `storm.thumbnail` | string |  |
| `storm.title` | string |  |
| `storm.votesperadmin` | number |  |
| `storm.votesperuser` | number |  |

## Native endpoint

Through the native Stormboard API, this operation is `POST /storms/join` (base URL `https://api.stormboard.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/join-storm.md) for the provider-specific parameters and requirements.

