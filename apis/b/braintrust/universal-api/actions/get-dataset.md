# Braintrust: Get Dataset

Retrieves a dataset from Braintrust.

```
GET https://connect.mindcloud.co/v1/universal/braintrust/latest/actions/get-dataset
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Braintrust `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/braintrust/latest/actions/get-dataset?connectionId=$CONNECTION_ID&datasetId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "datasetId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/braintrust/latest/actions/get-dataset?${params}`, {
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
| `datasetId` | string | yes | Dataset id. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Braintrust API returns.

## Native endpoint

Through the native Braintrust API, this operation is `GET /v1/dataset/:dataset_id` (base URL `https://api.braintrust.dev`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-dataset.md) for the provider-specific parameters and requirements.

