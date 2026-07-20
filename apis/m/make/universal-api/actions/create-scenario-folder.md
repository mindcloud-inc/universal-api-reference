# Make: Create Scenario Folder

Creates a scenario folder in the specified team.

```
POST https://connect.mindcloud.co/v1/universal/make/latest/actions/create-scenario-folder
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Make `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/make/latest/actions/create-scenario-folder" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "teamId": 1,
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/make/latest/actions/create-scenario-folder', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "teamId": 1,
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `teamId` | number | yes | The ID of the Make team in which to create the scenario folder. |
| `name` | string | yes | The name of the scenario folder to create. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "name": "Ava Chen",
      "scenariosTotal": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |
| `name` | string |  |
| `scenariosTotal` | number |  |

## Native endpoint

Through the native Make API, this operation is `POST /scenarios-folders` (base URL `https://us2.make.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-scenario-folder.md) for the provider-specific parameters and requirements.

