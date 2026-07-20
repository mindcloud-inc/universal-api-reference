# Omniconvert Explore: Start or Stop Experiment

Updates an experiment by starting or stopping it in Omniconvert Explore.

```
PUT https://connect.mindcloud.co/v1/universal/omniconvertExplore/latest/actions/start-or-stop-experiment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Omniconvert Explore `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/omniconvertExplore/latest/actions/start-or-stop-experiment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "action": "string",
  "experimentId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/omniconvertExplore/latest/actions/start-or-stop-experiment', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "action": "string",
    "experimentId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `action` | string | yes | Experiment action documented by Omniconvert. Allowed values: start, stop. |
| `experimentId` | number | yes | Identifier of the experiment taken from the experiments list. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Omniconvert Explore API returns.

## Native endpoint

Through the native Omniconvert Explore API, this operation is `POST /experiments/:experimentId/:action` (base URL `https://api.omniconvert.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/start-or-stop-experiment.md) for the provider-specific parameters and requirements.

