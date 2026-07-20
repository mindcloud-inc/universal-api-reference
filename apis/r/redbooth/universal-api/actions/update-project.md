# Redbooth: Update Project

Updates an existing project in Redbooth.

```
PUT https://connect.mindcloud.co/v1/universal/redbooth/latest/actions/update-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Redbooth `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/redbooth/latest/actions/update-project" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1,
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/redbooth/latest/actions/update-project', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1,
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | Redbooth project ID |
| `name` | string | yes | Updated project name |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archived": true,
      "id": 1,
      "name": "Ava Chen",
      "organization_id": 1,
      "permalink": "https://example.com",
      "project_id": 1,
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archived` | boolean |  |
| `id` | number |  |
| `name` | string |  |
| `organization_id` | number |  |
| `permalink` | string |  |
| `project_id` | number |  |
| `type` | string |  |

## Native endpoint

Through the native Redbooth API, this operation is `PUT /projects/:id` (base URL `https://redbooth.com/api/3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-project.md) for the provider-specific parameters and requirements.

