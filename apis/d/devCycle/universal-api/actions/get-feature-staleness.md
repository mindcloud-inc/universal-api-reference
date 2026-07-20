# DevCycle: Get Feature Staleness

Retrieves staleness details for a feature from DevCycle.

```
GET https://connect.mindcloud.co/v1/universal/devCycle/latest/actions/get-feature-staleness
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DevCycle `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/devCycle/latest/actions/get-feature-staleness?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/devCycle/latest/actions/get-feature-staleness?${params}`, {
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
| `project` | string | no | Project key. Default: `mindcloud`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "disabled": true,
      "featureId": "string",
      "key": "string",
      "name": "Ava Chen",
      "stale": true,
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `disabled` | boolean |  |
| `featureId` | string |  |
| `key` | string |  |
| `name` | string |  |
| `stale` | boolean |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native DevCycle API, this operation is `GET /v2/projects/:project/features/:feature/staleness` (base URL `https://api.devcycle.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-feature-staleness.md) for the provider-specific parameters and requirements.

