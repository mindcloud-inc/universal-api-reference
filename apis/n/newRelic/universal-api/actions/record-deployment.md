# New Relic: Record Deployment

Records a deployment in New Relic.

```
POST https://connect.mindcloud.co/v1/universal/newRelic/latest/actions/record-deployment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a New Relic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/newRelic/latest/actions/record-deployment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "appId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/newRelic/latest/actions/record-deployment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "appId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `appId` | number | yes | New Relic application ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "deployment": {
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
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `deployment.changelog` | string |  |
| `deployment.description` | string |  |
| `deployment.id` | number |  |
| `deployment.links.application` | number |  |
| `deployment.revision` | string |  |
| `deployment.timestamp` | date |  |
| `deployment.user` | string |  |

## Native endpoint

Through the native New Relic API, this operation is `POST /applications/:appId/deployments.json` (base URL `https://api.newrelic.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/record-deployment.md) for the provider-specific parameters and requirements.

