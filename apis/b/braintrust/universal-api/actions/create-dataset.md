# Braintrust: Create Dataset

Creates a new dataset in Braintrust.

```
POST https://connect.mindcloud.co/v1/universal/braintrust/latest/actions/create-dataset
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Braintrust `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/braintrust/latest/actions/create-dataset" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectId": "string",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/braintrust/latest/actions/create-dataset', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projectId": "string",
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `projectId` | string | yes | Project id. |
| `name` | string | yes | Dataset name. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Braintrust API returns.

## Native endpoint

Through the native Braintrust API, this operation is `POST /v1/dataset` (base URL `https://api.braintrust.dev`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-dataset.md) for the provider-specific parameters and requirements.

