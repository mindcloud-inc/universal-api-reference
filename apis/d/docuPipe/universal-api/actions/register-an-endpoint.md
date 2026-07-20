# DocuPipe: Register an Endpoint

Registers a webhook endpoint in DocuPipe.

```
POST https://connect.mindcloud.co/v1/universal/docuPipe/latest/actions/register-an-endpoint
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DocuPipe `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/docuPipe/latest/actions/register-an-endpoint" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/docuPipe/latest/actions/register-an-endpoint', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "url": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `url` | string | yes | The URL of the webhook endpoint |
| `subscribedEvents[]` | array<string> | no | The events to subscribe to, if not specified, all events will be sent to the endpoint |

## Response

```json
{
  "success": true,
  "data": [
    {
      "endpointId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `endpointId` | string | The ID which identifies the endpoint |

## Native endpoint

Through the native DocuPipe API, this operation is `POST /webhook/generate-endpoint` (base URL `https://app.docupipe.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/register-an-endpoint.md) for the provider-specific parameters and requirements.

