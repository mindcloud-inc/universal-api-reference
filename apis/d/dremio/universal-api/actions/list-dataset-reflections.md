# Dremio: List Dataset Reflections

Retrieves reflections for a dataset in Dremio.

```
GET https://connect.mindcloud.co/v1/universal/dremio/latest/actions/list-dataset-reflections
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dremio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dremio/latest/actions/list-dataset-reflections?connectionId=$CONNECTION_ID&datasetId=string&projectId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "datasetId": "string",
  "projectId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dremio/latest/actions/list-dataset-reflections?${params}`, {
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
| `datasetId` | string | yes |  |
| `projectId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "canAlterReflections": true,
      "data": [
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
| `canAlterReflections` | boolean |  |
| `data` | array<object> |  |

## Native endpoint

Through the native Dremio API, this operation is `GET /projects/:project_id/dataset/:datasetId/reflection` (base URL `https://api.dremio.cloud/v0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-dataset-reflections.md) for the provider-specific parameters and requirements.

