# Synthflow AI Phone Calling: Create Simulation Case

Creates a new simulation case in Synthflow.

```
POST https://connect.mindcloud.co/v1/universal/synthflowAIPhoneCalling/latest/actions/create-simulation-case
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Synthflow AI Phone Calling `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/synthflowAIPhoneCalling/latest/actions/create-simulation-case" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/synthflowAIPhoneCalling/latest/actions/create-simulation-case', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Synthflow AI Phone Calling API returns.

## Native endpoint

Through the native Synthflow AI Phone Calling API, this operation is `POST /simulation_cases` (base URL `https://api.synthflow.ai/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-simulation-case.md) for the provider-specific parameters and requirements.

