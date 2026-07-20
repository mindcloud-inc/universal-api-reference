# Microsoft Power BI: Datasets PostDataset



```
POST https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/push-datasets-datasets-postdataset
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft Power BI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/push-datasets-datasets-postdataset" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "tables[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/push-datasets-datasets-postdataset', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "tables[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `defaultRetentionPolicy` | object | no | The default retention policy |
| `name` | string | yes | The dataset name |
| `tables[]` | array<object> | yes | The dataset tables |
| `datasources[]` | array<object> | no | The data sources associated with this dataset |
| `defaultMode` | object | no | The dataset mode or type |
| `relationships[]` | array<object> | no | The dataset relationships |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Microsoft Power BI API returns.

## Native endpoint

Through the native Microsoft Power BI API, this operation is `POST datasets` (base URL `https://api.powerbi.com/v1.0/myorg`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/push-datasets-datasets-postdataset.md) for the provider-specific parameters and requirements.

