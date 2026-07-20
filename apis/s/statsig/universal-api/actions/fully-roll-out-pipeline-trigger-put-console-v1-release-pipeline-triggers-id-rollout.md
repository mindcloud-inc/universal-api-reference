# Statsig: Fully Roll Out Pipeline Trigger

Fully rolls out a pipeline trigger in Statsig.

```
PUT https://connect.mindcloud.co/v1/universal/statsig/latest/actions/fully-roll-out-pipeline-trigger-put-console-v1-release-pipeline-triggers-id-rollout
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Statsig `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/statsig/latest/actions/fully-roll-out-pipeline-trigger-put-console-v1-release-pipeline-triggers-id-rollout" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/statsig/latest/actions/fully-roll-out-pipeline-trigger-put-console-v1-release-pipeline-triggers-id-rollout', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Statsig response data payload. |
| `message` | string | Statsig response message. |

## Native endpoint

Through the native Statsig API, this operation is `PUT /console/v1/release_pipeline_triggers/{id}/rollout` (base URL `https://statsigapi.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/fully-roll-out-pipeline-trigger-put-console-v1-release-pipeline-triggers-id-rollout.md) for the provider-specific parameters and requirements.

