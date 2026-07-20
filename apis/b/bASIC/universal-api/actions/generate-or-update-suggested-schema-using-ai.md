# BASIC: Generate or update suggested schema using AI

Generates or updates a suggested schema with AI in BASIC.

```
PUT https://connect.mindcloud.co/v1/universal/bASIC/latest/actions/generate-or-update-suggested-schema-using-ai
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BASIC `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/bASIC/latest/actions/generate-or-update-suggested-schema-using-ai" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bASIC/latest/actions/generate-or-update-suggested-schema-using-ai', {
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
      "schema": {
        "project_id": "string",
        "tables": {},
        "version": 1
      },
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `schema.project_id` | string |  |
| `schema.tables` | object |  |
| `schema.version` | number |  |
| `success` | boolean |  |

## Native endpoint

Through the native BASIC API, this operation is `POST /project/{id}/schema/generate` (base URL `https://api.basic.tech`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-or-update-suggested-schema-using-ai.md) for the provider-specific parameters and requirements.

