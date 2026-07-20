# Cloud 66: Get SSL Certificate

Retrieves an SSL certificate from your Cloud 66 account.

```
GET https://connect.mindcloud.co/v1/universal/cloud66/latest/actions/get-ssl-certificate
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cloud 66 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cloud66/latest/actions/get-ssl-certificate?connectionId=$CONNECTION_ID&stackId=string&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "stackId": "string",
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cloud66/latest/actions/get-ssl-certificate?${params}`, {
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
| `stackId` | string | yes | Unique identifier of the stack |
| `id` | string | yes | SSL certificate ID |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Cloud 66 API returns.

## Native endpoint

Through the native Cloud 66 API, this operation is `GET /stacks/:stack_id/ssl_certificates/:id` (base URL `https://app.cloud66.com/api/3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-ssl-certificate.md) for the provider-specific parameters and requirements.

