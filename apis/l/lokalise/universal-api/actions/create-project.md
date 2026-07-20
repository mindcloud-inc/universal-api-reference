# Lokalise: Create Project

Creates a new project in Lokalise.

```
POST https://connect.mindcloud.co/v1/universal/lokalise/latest/actions/create-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lokalise `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/lokalise/latest/actions/create-project" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/lokalise/latest/actions/create-project', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "base_language_iso": "string",
      "description": "string",
      "name": "Ava Chen",
      "project_id": "string",
      "project_type": "string",
      "team_id": 1,
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `base_language_iso` | string |  |
| `description` | string |  |
| `name` | string |  |
| `project_id` | string |  |
| `project_type` | string |  |
| `team_id` | number |  |
| `uuid` | string |  |

## Native endpoint

Through the native Lokalise API, this operation is `POST /projects` (base URL `https://api.lokalise.com/api2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-project.md) for the provider-specific parameters and requirements.

