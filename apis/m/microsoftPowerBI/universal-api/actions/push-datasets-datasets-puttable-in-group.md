# Microsoft Power BI: Datasets PutTableInGroup



```
PUT https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/push-datasets-datasets-puttable-in-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft Power BI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/push-datasets-datasets-puttable-in-group" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "groupId": "string",
  "datasetId": "string",
  "tableName": "Ava Chen",
  "columns[]": [
    {}
  ],
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/push-datasets-datasets-puttable-in-group', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "groupId": "string",
    "datasetId": "string",
    "tableName": "Ava Chen",
    "columns[]": [{}],
    "name": "Ava Chen"
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
| `tableName` | string | yes | The table name |
| `columns[]` | array<object> | yes | The column schema for this table |
| `name` | string | yes | The table name |
| `description` | string | no | The table description |
| `isHidden` | boolean | no | Optional. Whether this dataset table is hidden. |
| `measures[]` | array<object> | no | The measures within this table |
| `rows[]` | array<object> | no | The data rows within this table |
| `source[]` | array<object> | no | The table source |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Microsoft Power BI API returns.

## Native endpoint

Through the native Microsoft Power BI API, this operation is `PUT groups/[:groupId]/datasets/[:datasetId]/tables/[:tableName]` (base URL `https://api.powerbi.com/v1.0/myorg`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/push-datasets-datasets-puttable-in-group.md) for the provider-specific parameters and requirements.

