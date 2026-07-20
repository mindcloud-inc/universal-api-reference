# Neon: Create project

Creates a project in Neon.

```
POST https://connect.mindcloud.co/v1/universal/neon/latest/actions/create-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Neon `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/neon/latest/actions/create-project" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "project": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/neon/latest/actions/create-project', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "project": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `project` | object | yes | Neon API parameter project |

## Response

```json
{
  "success": true,
  "data": [
    {
      "branch": {},
      "connection_uris": [
        {}
      ],
      "databases": [
        {}
      ],
      "endpoints": [
        {}
      ],
      "operations": [
        {}
      ],
      "project": {},
      "roles": [
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
| `branch` | object |  |
| `connection_uris` | array<object> |  |
| `databases` | array<object> |  |
| `endpoints` | array<object> |  |
| `operations` | array<object> |  |
| `project` | object |  |
| `roles` | array<object> |  |

## Native endpoint

Through the native Neon API, this operation is `POST /projects` (base URL `https://console.neon.tech/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-project.md) for the provider-specific parameters and requirements.

