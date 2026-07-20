# ID Analyzer: Create a hosted Docupass flow

Creates a hosted Docupass flow in ID Analyzer.

```
POST https://connect.mindcloud.co/v1/universal/iDAnalyzer/latest/actions/create-a-hosted-docupass-flow
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ID Analyzer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/iDAnalyzer/latest/actions/create-a-hosted-docupass-flow" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "mode": "1",
  "profile": "string",
  "version": "3"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/iDAnalyzer/latest/actions/create-a-hosted-docupass-flow', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "mode": "1",
    "profile": "string",
    "version": "3"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `mode` | number | yes | Docupass flow mode. Default: `1`. |
| `profile` | string | yes | KYC profile ID configured for Docupass. |
| `version` | string | yes | Docupass version. Default: `3`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native ID Analyzer API returns.

## Native endpoint

Through the native ID Analyzer API, this operation is `POST /docupass` (base URL `https://api2.idanalyzer.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-a-hosted-docupass-flow.md) for the provider-specific parameters and requirements.

