# Docutray: Start Step Execution



```
POST https://connect.mindcloud.co/v1/universal/docutray/latest/actions/execute-step-async
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Docutray `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/docutray/latest/actions/execute-step-async" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "stepId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/docutray/latest/actions/execute-step-async', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "stepId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `documentMetadata` | object | no | Optional metadata returned with the step execution result |
| `imageBase64` | string | no | Base64-encoded image or PDF content |
| `imageContentType` | string | no | Optional MIME type when Docutray cannot infer it |
| `imageUrl` | string | no | HTTP or HTTPS URL of the image or PDF to process |
| `stepId` | string | yes | Step ID for processing |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Docutray API returns.

## Native endpoint

Through the native Docutray API, this operation is `POST api/steps-async/:stepId` (base URL `https://app.docutray.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/execute-step-async.md) for the provider-specific parameters and requirements.

