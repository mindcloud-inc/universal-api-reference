# DevCycle: Get Environment

Retrieves an environment from DevCycle.

```
GET https://connect.mindcloud.co/v1/universal/devCycle/latest/actions/get-environment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DevCycle `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/devCycle/latest/actions/get-environment?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/devCycle/latest/actions/get-environment?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `key` | string | no | Environment key. Default: `development`. |
| `project` | string | no | Project key. Default: `mindcloud`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "color": "string",
      "createdAt": "string",
      "createdBy": "string",
      "id": "string",
      "key": "string",
      "name": "Ava Chen",
      "projectId": "string",
      "readonly": true,
      "sdkKeys": {
        "client": [
          [
            {}
          ]
        ],
        "mobile": [
          [
            {}
          ]
        ],
        "server": [
          [
            {}
          ]
        ]
      },
      "type": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `color` | string |  |
| `createdAt` | string |  |
| `createdBy` | string |  |
| `id` | string |  |
| `key` | string |  |
| `name` | string |  |
| `projectId` | string |  |
| `readonly` | boolean |  |
| `sdkKeys.client[]` | array<object> |  |
| `sdkKeys.mobile[]` | array<object> |  |
| `sdkKeys.server[]` | array<object> |  |
| `type` | string |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native DevCycle API, this operation is `GET /v1/projects/:project/environments/:key` (base URL `https://api.devcycle.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-environment.md) for the provider-specific parameters and requirements.

