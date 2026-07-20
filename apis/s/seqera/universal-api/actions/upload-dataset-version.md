# Seqera: Upload Dataset Version

Uploads a new dataset version to Seqera.

```
POST https://connect.mindcloud.co/v1/universal/seqera/latest/actions/upload-dataset-version
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Seqera `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/seqera/latest/actions/upload-dataset-version" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "workspaceId": 1,
  "datasetId": "string",
  "file": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/seqera/latest/actions/upload-dataset-version', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "workspaceId": 1,
    "datasetId": "string",
    "file": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `workspaceId` | number | yes |  |
| `datasetId` | string | yes |  |
| `header` | boolean | no |  |
| `file` | file | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Seqera API returns.

## Native endpoint

Through the native Seqera API, this operation is `POST /workspaces/:workspaceId/datasets/:datasetId/upload` (base URL `https://api.cloud.seqera.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-dataset-version.md) for the provider-specific parameters and requirements.

