# Databricks: List Pipelines

Retrieves pipelines from the Databricks workspace.

```
GET https://connect.mindcloud.co/v1/universal/databricks/latest/actions/list-pipelines
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Databricks `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/databricks/latest/actions/list-pipelines?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/databricks/latest/actions/list-pipelines?${params}`, {
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
| `pageToken` | string | no | Page token returned by previous call |
| `maxResults` | number | no | The maximum number of entries to return in a single page. The system may return fewer than max_results events in a response, even if there are more events available. This field is optional. The default value is 25. The maximum value is 100. An error is returned if the value of max_results is greater than 100. |
| `orderBy` | list<string> | no | A list of strings specifying the order of results. Supported order_by fields are id and name. The default is id asc. This field is optional. |
| `filter` | string | no | Select a subset of results based on the specified criteria. The supported filters are: * `notebook='<path>'` to select pipelines that reference the provided notebook path. * `name LIKE '[pattern]'` to select pipelines with a name that matches pattern. Wildcards are supported, for example: `name LIKE '%shopping%'` Composite filters are not supported. This field is optional. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cluster_id": "string",
      "creator_user_name": "Ava Chen",
      "health": "string",
      "latest_updates": [
        {
          "creation_time": "string",
          "state": "string",
          "update_id": "string"
        }
      ],
      "name": "Ava Chen",
      "pipeline_id": "string",
      "run_as_user_name": "Ava Chen",
      "state": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cluster_id` | string | The unique identifier of the cluster running the pipeline. |
| `creator_user_name` | string | The username of the pipeline creator. |
| `health` | string | The health of a pipeline. |
| `latest_updates` | array<string> | Status of the latest updates for the pipeline. Ordered with the newest update first. |
| `latest_updates[].creation_time` | string |  |
| `latest_updates[].state` | string | The update state. |
| `latest_updates[].update_id` | string |  |
| `name` | string | The user-friendly name of the pipeline. |
| `pipeline_id` | string | The unique identifier of the pipeline. |
| `run_as_user_name` | string | The username that the pipeline runs as. This is a read only value derived from the pipeline owner. |
| `state` | string | The pipeline state. |

## Native endpoint

Through the native Databricks API, this operation is `GET {{credentials.host}}/api/2.0/pipelines` (base URL `https://accounts.cloud.databricks.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-pipelines.md) for the provider-specific parameters and requirements.

