# Currents: Generate Test Signature



```
POST https://connect.mindcloud.co/v1/universal/currents/latest/actions/generate-test-signature
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Currents `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/currents/latest/actions/generate-test-signature" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectId": "string",
  "specFilePath": "string",
  "testTitle": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/currents/latest/actions/generate-test-signature', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projectId": "string",
    "specFilePath": "string",
    "testTitle": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `projectId` | string | yes |  |
| `specFilePath` | string | yes |  |
| `testTitle` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "signature": "string"
      },
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.signature` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Currents API, this operation is `POST /signature/test` (base URL `https://api.currents.dev/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-test-signature.md) for the provider-specific parameters and requirements.

