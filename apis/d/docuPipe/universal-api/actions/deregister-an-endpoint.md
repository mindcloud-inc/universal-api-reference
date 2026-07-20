# DocuPipe: Deregister an Endpoint

Deletes a webhook endpoint from DocuPipe.

```
DELETE https://connect.mindcloud.co/v1/universal/docuPipe/latest/actions/deregister-an-endpoint
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DocuPipe `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/docuPipe/latest/actions/deregister-an-endpoint?connectionId=$CONNECTION_ID&endpointId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "endpointId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/docuPipe/latest/actions/deregister-an-endpoint?${params}`, {
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
| `endpointId` | string | yes | The ID which identifies the webhook endpoint |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean | The webhook endpoint was successfully deleted |

## Native endpoint

Through the native DocuPipe API, this operation is `POST /webhook/delete-endpoint` (base URL `https://app.docupipe.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/deregister-an-endpoint.md) for the provider-specific parameters and requirements.

