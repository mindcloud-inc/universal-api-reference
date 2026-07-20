# Microsoft Power BI: Execute Dax Queries In Group



```
POST https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/datasets-execute-dax-queries-in-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft Power BI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/datasets-execute-dax-queries-in-group" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "groupId": "string",
  "datasetId": "string",
  "query": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/datasets-execute-dax-queries-in-group', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "groupId": "string",
    "datasetId": "string",
    "query": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `groupId` | string | yes | The workspace ID |
| `datasetId` | string | yes | The dataset ID |
| `query` | string | yes | Query text. |
| `applicationContext` | string | no | JSON structure containing additional information about an operation. |
| `culture` | string | no | Culture code that controls locale-specific query formatting, such as en-US. For more information about supported culture codes, see Supported languages and countries/regions for Power BI. |
| `customData` | string | no | Custom data for use in Dynamic RLS. For example, North America can be referenced by the model's CUSTOMDATA() function. |
| `effectiveUsername` | string | no | Effective username for the query. |
| `memoryLimit` | number | no | Memory limit (in KB) for the query. |
| `queryTimeout` | number | no | Query timeout in seconds. |
| `resultSetRowCountLimit` | number | no | Maximum number of rows to return. Default is 1,000,000 rows. |
| `roles[]` | array<string> | no | Roles assigned to the user. |
| `schemaOnly` | boolean | no | Whether the query must return only the schema. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Microsoft Power BI API returns.

## Native endpoint

Through the native Microsoft Power BI API, this operation is `POST groups/[:groupId]/datasets/[:datasetId]/executeDaxQueries` (base URL `https://api.powerbi.com/v1.0/myorg`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/datasets-execute-dax-queries-in-group.md) for the provider-specific parameters and requirements.

