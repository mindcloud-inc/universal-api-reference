# DevCycle: Get Feature Variation

Retrieves a feature variation from DevCycle.

```
GET https://connect.mindcloud.co/v1/universal/devCycle/latest/actions/get-feature-variation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DevCycle `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/devCycle/latest/actions/get-feature-variation?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/devCycle/latest/actions/get-feature-variation?${params}`, {
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
| `feature` | string | no | Feature key. Default: `mindcloud-flag`. |
| `key` | string | no | Variation key. Default: `on`. |
| `project` | string | no | Project key. Default: `mindcloud`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "key": "string",
      "name": "Ava Chen",
      "variables": [
        [
          {}
        ]
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `key` | string |  |
| `name` | string |  |
| `variables[]` | array<object> |  |

## Native endpoint

Through the native DevCycle API, this operation is `GET /v1/projects/:project/features/:feature/variations/:key` (base URL `https://api.devcycle.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-feature-variation.md) for the provider-specific parameters and requirements.

