# BASIC: Update project schema

Updates a project schema in BASIC.

```
PUT https://connect.mindcloud.co/v1/universal/bASIC/latest/actions/update-project-schema
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BASIC `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/bASIC/latest/actions/update-project-schema" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bASIC/latest/actions/update-project-schema', {
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



## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "id": "string",
        "project_id": "string",
        "schema": {},
        "updated_at": "2026-05-07T12:00:00.000Z"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.id` | string |  |
| `data.project_id` | string |  |
| `data.schema` | object |  |
| `data.updated_at` | date |  |

## Native endpoint

Through the native BASIC API, this operation is `POST /project/{id}/schema` (base URL `https://api.basic.tech`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-project-schema.md) for the provider-specific parameters and requirements.

