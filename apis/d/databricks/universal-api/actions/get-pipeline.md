# Databricks: Get Pipeline

Retrieves a pipeline from the Databricks workspace.

```
GET https://connect.mindcloud.co/v1/universal/databricks/latest/actions/get-pipeline
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Databricks `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/databricks/latest/actions/get-pipeline?connectionId=$CONNECTION_ID&pipelineId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "pipelineId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/databricks/latest/actions/get-pipeline?${params}`, {
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
| `pipelineId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "creation_time": "string",
      "state": "string",
      "update_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `creation_time` | string |  |
| `state` | string | The update state. |
| `update_id` | string |  |

## Native endpoint

Through the native Databricks API, this operation is `GET {{credentials.host}}/api/2.0/pipelines/:pipelineId` (base URL `https://accounts.cloud.databricks.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-pipeline.md) for the provider-specific parameters and requirements.

