# Neon: Restart compute endpoint

Restarts compute endpoint in Neon.

```
POST https://connect.mindcloud.co/v1/universal/neon/latest/actions/restart-project-endpoint
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Neon `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/neon/latest/actions/restart-project-endpoint" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "project_id": "string",
  "endpoint_id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/neon/latest/actions/restart-project-endpoint', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "project_id": "string",
    "endpoint_id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `project_id` | string | yes | Neon API parameter project_id |
| `endpoint_id` | string | yes | Neon API parameter endpoint_id |

## Response

```json
{
  "success": true,
  "data": [
    {
      "endpoint": {},
      "operations": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `endpoint` | object |  |
| `operations` | array<object> |  |

## Native endpoint

Through the native Neon API, this operation is `POST /projects/:project_id/endpoints/:endpoint_id/restart` (base URL `https://console.neon.tech/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/restart-project-endpoint.md) for the provider-specific parameters and requirements.

