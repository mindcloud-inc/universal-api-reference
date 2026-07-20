# HoneyHive: Add Datapoints

Adds datapoints to a dataset in HoneyHive.

```
POST https://connect.mindcloud.co/v1/universal/honeyHive/latest/actions/add-datapoints
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HoneyHive `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/honeyHive/latest/actions/add-datapoints" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "datasetId": "string",
  "project": "string",
  "data[]": [
    {}
  ],
  "mapping": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/honeyHive/latest/actions/add-datapoints', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "datasetId": "string",
    "project": "string",
    "data[]": [{}],
    "mapping": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `datasetId` | string | yes | Dataset ID to add datapoints to. |
| `project` | string | yes | Project name. |
| `data[]` | array<object> | yes | Data rows to add as datapoints. |
| `mapping` | object | yes | Mapping for inputs, ground truth, and history. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "datapointIds": [
        "string"
      ],
      "inserted": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `datapointIds` | array<string> |  |
| `inserted` | number |  |

## Native endpoint

Through the native HoneyHive API, this operation is `POST /datasets/{dataset_id}/datapoints` (base URL `https://api.honeyhive.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-datapoints.md) for the provider-specific parameters and requirements.

