# Databricks: Start Pipeline Update

Starts a pipeline update in Databricks.

```
POST https://connect.mindcloud.co/v1/universal/databricks/latest/actions/start-pipeline-update
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Databricks `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/databricks/latest/actions/start-pipeline-update" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "pipelineId": "string",
  "fullRefreshSelection": "string",
  "refreshSelection": "string",
  "resetCheckpointSelection": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/databricks/latest/actions/start-pipeline-update', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "pipelineId": "string",
    "fullRefreshSelection": "string",
    "refreshSelection": "string",
    "resetCheckpointSelection": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `pipelineId` | string | yes |  |
| `cause` | string | no | What triggered this update. |
| `fullRefresh` | boolean | no | If true, this update will reset all tables before running. |
| `fullRefreshSelection` | list<string> | yes | A list of tables to update with fullRefresh. If both refresh_selection and full_refresh_selection are empty, this is a full graph update. Full Refresh on a table means that the states of the table will be reset before the refresh. |
| `refreshSelection` | list<string> | yes | A list of tables to update without fullRefresh. If both refresh_selection and full_refresh_selection are empty, this is a full graph update. Full Refresh on a table means that the states of the table will be reset before the refresh. |
| `resetCheckpointSelection` | list<string> | yes | A list of flows for which this update should reset the streaming checkpoint. This selection will not clear the data in the flow's target table. Flows in this list may also appear in refresh_selection and full_refresh_selection. |
| `validateOnly` | boolean | no | If true, this update only validates the correctness of pipeline source code but does not materialize or publish any datasets. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "update_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `update_id` | string |  |

## Native endpoint

Through the native Databricks API, this operation is `POST {{credentials.host}}/api/2.0/pipelines/:pipelineId/updates` (base URL `https://accounts.cloud.databricks.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/start-pipeline-update.md) for the provider-specific parameters and requirements.

