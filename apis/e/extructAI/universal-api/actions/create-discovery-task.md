# Extruct AI: Create Discovery Task

Creates a discovery task in Extruct AI.

```
POST https://connect.mindcloud.co/v1/universal/extructAI/latest/actions/create-discovery-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Extruct AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/extructAI/latest/actions/create-discovery-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "query": "vertical SaaS companies serving freight forwarding"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/extructAI/latest/actions/create-discovery-task', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "query": "vertical SaaS companies serving freight forwarding"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `query` | string | yes | Natural-language description of companies to find. Example: `vertical SaaS companies serving freight forwarding`. |
| `desiredNumResults` | number | no | Target number of results for this task. Default: `100`. Example: `100`. |
| `autoDataSources` | boolean | no | Automatically determine the best data sources. Default: `true`. Example: `true`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `dataSources` | list<string> | no | Manual data source selection. One of: `LinkedIn`, `Maps`, `Web Search`. Accepts multiple values as an array. Example: `web_search`. |
| `table` | object | no | Optional table settings for this discovery task. |
| `table.id` | string | no | Existing table identifier. Example: `3c90c3cc-0d44-4b50-8888-8dd25736052a`. |
| `table.run` | boolean | no | Whether to run the table workflow. Example: `false`. |
| `table.columns[]` | array<string> | no | Table column identifiers. |
| `table.autoImport` | boolean | no | Whether to auto import task results into the table. Example: `false`. |
| `criteria[]` | array<object> | no | Optional criteria definitions used to score results. |
| `criteria[].key` | string | no | Criterion key. Example: `buyer_focus`. |
| `criteria[].name` | string | no | Criterion display name. Example: `Buyer Focus`. |
| `criteria[].criterion` | string | no | Criterion text. Example: `Sells to freight forwarding teams`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "autoDataSources": true,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "criteria": [
        {}
      ],
      "dataSources": [
        "string"
      ],
      "desiredNumResults": 1,
      "id": "string",
      "isExhausted": true,
      "numResults": 1,
      "numResultsDiscovered": 1,
      "numResultsEnriched": 1,
      "numResultsEvaluated": 1,
      "query": "string",
      "status": "string",
      "tableId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `autoDataSources` | boolean |  |
| `createdAt` | date |  |
| `criteria` | array<object> |  |
| `dataSources` | array<string> |  |
| `desiredNumResults` | number |  |
| `id` | string |  |
| `isExhausted` | boolean |  |
| `numResults` | number |  |
| `numResultsDiscovered` | number |  |
| `numResultsEnriched` | number |  |
| `numResultsEvaluated` | number |  |
| `query` | string |  |
| `status` | string |  |
| `tableId` | string |  |

## Native endpoint

Through the native Extruct AI API, this operation is `POST /v1/discovery_tasks` (base URL `https://api.extruct.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-discovery-task.md) for the provider-specific parameters and requirements.

