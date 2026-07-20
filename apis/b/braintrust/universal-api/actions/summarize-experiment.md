# Braintrust: Summarize Experiment

Retrieves a summary of an experiment in Braintrust.

```
GET https://connect.mindcloud.co/v1/universal/braintrust/latest/actions/summarize-experiment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Braintrust `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/braintrust/latest/actions/summarize-experiment?connectionId=$CONNECTION_ID&experimentId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "experimentId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/braintrust/latest/actions/summarize-experiment?${params}`, {
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
| `experimentId` | string | yes | Experiment id. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Braintrust API returns.

## Native endpoint

Through the native Braintrust API, this operation is `GET /v1/experiment/:experiment_id/summarize` (base URL `https://api.braintrust.dev`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/summarize-experiment.md) for the provider-specific parameters and requirements.

