# Hex: Run Project



```
POST https://connect.mindcloud.co/v1/universal/hex/latest/actions/run-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hex `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/hex/latest/actions/run-project" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hex/latest/actions/run-project', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projectId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `dryRun` | boolean | no | Whether to trigger the project run as a dry run. |
| `projectId` | string | yes | Unique ID for a Hex project. |
| `updateCache` | boolean | no |  |
| `updatePublishedResults` | boolean | no |  |
| `useCachedSqlResults` | boolean | no |  |
| `viewId` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "notifications": [
        {}
      ],
      "projectId": "string",
      "projectVersion": 1,
      "runId": "string",
      "runStatusUrl": "https://example.com",
      "runUrl": "https://example.com",
      "traceId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `notifications` | array<object> | Deletes an existing group from Hex. |
| `projectId` | string |  |
| `projectVersion` | number |  |
| `runId` | string |  |
| `runStatusUrl` | string |  |
| `runUrl` | string |  |
| `traceId` | string |  |

## Native endpoint

Through the native Hex API, this operation is `POST /projects/:projectId/runs` (base URL `https://app.hex.tech/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/run-project.md) for the provider-specific parameters and requirements.

