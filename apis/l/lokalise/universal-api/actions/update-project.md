# Lokalise: Update Project

Updates an existing project in Lokalise.

```
PUT https://connect.mindcloud.co/v1/universal/lokalise/latest/actions/update-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lokalise `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/lokalise/latest/actions/update-project" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/lokalise/latest/actions/update-project', {
  method: 'PUT',
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

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `project_id` | string | no | Lokalise project identifier. |

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

Through the native Lokalise API, this operation is `PUT /projects/:project_id` (base URL `https://api.lokalise.com/api2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-project.md) for the provider-specific parameters and requirements.

