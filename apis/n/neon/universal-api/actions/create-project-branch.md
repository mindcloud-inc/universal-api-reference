# Neon: Create branch

Creates a branch in Neon.

```
POST https://connect.mindcloud.co/v1/universal/neon/latest/actions/create-project-branch
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Neon `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/neon/latest/actions/create-project-branch" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "project_id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/neon/latest/actions/create-project-branch', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "project_id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `project_id` | string | yes | Neon API parameter project_id |
| `endpoints[]` | array<object> | no | Neon API parameter endpoints |
| `branch` | object | no | Neon API parameter branch |
| `annotation_value` | object | no | Neon API parameter annotation_value |

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
| `roles` | array<object> |  |

## Native endpoint

Through the native Neon API, this operation is `POST /projects/:project_id/branches` (base URL `https://console.neon.tech/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-project-branch.md) for the provider-specific parameters and requirements.

