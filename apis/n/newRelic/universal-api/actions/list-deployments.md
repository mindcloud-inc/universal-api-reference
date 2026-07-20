# New Relic: List Deployments

Retrieves deployments from New Relic.

```
GET https://connect.mindcloud.co/v1/universal/newRelic/latest/actions/list-deployments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a New Relic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/newRelic/latest/actions/list-deployments?connectionId=$CONNECTION_ID&appId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "appId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/newRelic/latest/actions/list-deployments?${params}`, {
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
| `appId` | number | yes | New Relic application ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "deployments": [
        {
          "changelog": "string",
          "description": "string",
          "id": 1,
          "links": {
            "application": 1
          },
          "revision": "string",
          "timestamp": "2026-05-07T12:00:00.000Z",
          "user": "string"
        }
      ],
      "links": {
        "deployment": {
          "agent": "https://example.com"
        }
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `deployments[].changelog` | string |  |
| `deployments[].description` | string |  |
| `deployments[].id` | number |  |
| `deployments[].links.application` | number |  |
| `deployments[].revision` | string |  |
| `deployments[].timestamp` | date |  |
| `deployments[].user` | string |  |
| `links.deployment.agent` | string |  |

## Native endpoint

Through the native New Relic API, this operation is `GET /applications/:appId/deployments.json` (base URL `https://api.newrelic.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-deployments.md) for the provider-specific parameters and requirements.

