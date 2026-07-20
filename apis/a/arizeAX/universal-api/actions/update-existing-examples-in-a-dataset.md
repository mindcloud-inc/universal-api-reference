# Arize AX: Update Existing Examples In A Dataset

Updates existing examples in a dataset in Arize AX.

```
PUT https://connect.mindcloud.co/v1/universal/arizeAX/latest/actions/update-existing-examples-in-a-dataset
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Arize AX `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/arizeAX/latest/actions/update-existing-examples-in-a-dataset" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "datasetId": "string",
  "examples[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/arizeAX/latest/actions/update-existing-examples-in-a-dataset', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "datasetId": "string",
    "examples[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `datasetId` | string | yes |  |
| `examples[]` | array<object> | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Arize AX API returns.

## Native endpoint

Through the native Arize AX API, this operation is `PATCH /v2/datasets/:dataset_id/examples` (base URL `https://api.arize.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-existing-examples-in-a-dataset.md) for the provider-specific parameters and requirements.

