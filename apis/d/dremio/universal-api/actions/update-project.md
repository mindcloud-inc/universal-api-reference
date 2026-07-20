# Dremio: Update Project

Updates an existing project in Dremio.

```
PUT https://connect.mindcloud.co/v1/universal/dremio/latest/actions/update-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dremio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/dremio/latest/actions/update-project" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "project": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dremio/latest/actions/update-project', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "project": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes |  |
| `project` | object | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cloudId": "string",
      "createdBy": "string",
      "id": "string",
      "name": "Ava Chen",
      "state": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cloudId` | string |  |
| `createdBy` | string |  |
| `id` | string |  |
| `name` | string |  |
| `state` | string |  |

## Native endpoint

Through the native Dremio API, this operation is `PUT /projects/:id` (base URL `https://api.dremio.cloud/v0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-project.md) for the provider-specific parameters and requirements.

