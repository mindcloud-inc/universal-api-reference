# Cloud 66: List SSL Certificates

Retrieves SSL certificates from your Cloud 66 account.

```
GET https://connect.mindcloud.co/v1/universal/cloud66/latest/actions/list-ssl-certificates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cloud 66 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cloud66/latest/actions/list-ssl-certificates?connectionId=$CONNECTION_ID&stackId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "stackId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cloud66/latest/actions/list-ssl-certificates?${params}`, {
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

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Cloud 66 API returns.

## Native endpoint

Through the native Cloud 66 API, this operation is `GET /stacks/:stack_id/ssl_certificates` (base URL `https://app.cloud66.com/api/3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-ssl-certificates.md) for the provider-specific parameters and requirements.

