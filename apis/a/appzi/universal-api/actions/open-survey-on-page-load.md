# Appzi: Open Survey On Page Load

Generates an Appzi page-load survey trigger snippet.

```
POST https://connect.mindcloud.co/v1/universal/appzi/latest/actions/open-survey-on-page-load
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Appzi `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/appzi/latest/actions/open-survey-on-page-load" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "configId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/appzi/latest/actions/open-survey-on-page-load', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "configId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `configId` | string | yes | Survey configuration ID inserted into the generated page-load trigger snippet. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Appzi API returns.

## Native endpoint

Through the native Appzi API, this operation is `GET https://docs.appzi.io/integration/triggering-surveys/` (base URL `https://api.appzi.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/open-survey-on-page-load.md) for the provider-specific parameters and requirements.

