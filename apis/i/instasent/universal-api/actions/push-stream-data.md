# Instasent: Push Stream Data



```
POST https://connect.mindcloud.co/v1/universal/instasent/latest/actions/push-stream-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Instasent `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/instasent/latest/actions/push-stream-data" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "project": "string",
  "datasource": "string",
  "action": "string",
  "records[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/instasent/latest/actions/push-stream-data', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "project": "string",
    "datasource": "string",
    "action": "string",
    "records[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `project` | string | yes | Instasent project uid. Use the uid value from List Projects, not the internal project id. |
| `datasource` | string | yes | Datasource identifier. |
| `action` | string | yes | Stream action name. |
| `records[]` | array<object> | yes | Stream records to push. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `sync` | boolean | no | Whether to process the stream request synchronously. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accepted": [
        {
          "item": {},
          "position": 1
        }
      ],
      "apiSpeedTier": 1,
      "datasourceId": "string",
      "datasourceUid": "string",
      "dryRun": true,
      "entitiesFailures": 1,
      "entitiesLimit": 1,
      "entitiesSuccess": 1,
      "errors": [
        {
          "error": "string",
          "item": {},
          "position": 1
        }
      ],
      "projectId": "string",
      "projectUid": "string",
      "stats": {
        "callsFailures": 1,
        "callsSuccess": 1,
        "callsTotal": 1,
        "entitiesFailures": 1,
        "entitiesSuccess": 1
      },
      "status": 1,
      "streamId": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accepted[].item` | object | Submitted item that was accepted for processing |
| `accepted[].position` | number | Index of the accepted item in the submitted batch |
| `apiSpeedTier` | number | Applied API speed tier |
| `datasourceId` | string | Internal datasource identifier |
| `datasourceUid` | string | Datasource UID |
| `dryRun` | boolean | Whether dry-run mode was used |
| `entitiesFailures` | number | Number of failed entities |
| `entitiesLimit` | number | Batch entity limit applied by the API |
| `entitiesSuccess` | number | Number of successfully processed entities |
| `errors[].error` | string | Validation or processing error message |
| `errors[].item` | object | Submitted item that failed processing |
| `errors[].position` | number | Index of the failed item in the submitted batch |
| `projectId` | string | Internal project identifier |
| `projectUid` | string | Project UID used by the API |
| `stats.callsFailures` | number | Failed downstream processing calls |
| `stats.callsSuccess` | number | Successful downstream processing calls |
| `stats.callsTotal` | number | Total downstream processing calls |
| `stats.entitiesFailures` | number | Failed entity operations in processing stats |
| `stats.entitiesSuccess` | number | Successful entity operations in processing stats |
| `status` | number | HTTP status code |
| `streamId` | string | Resolved stream identifier |
| `success` | boolean | Whether the stream push operation was successful |

## Native endpoint

Through the native Instasent API, this operation is `POST /project/:project/datasource/:datasource/stream/:action` (base URL `https://api.instasent.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/push-stream-data.md) for the provider-specific parameters and requirements.

