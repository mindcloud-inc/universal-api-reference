# Sign.Plus: Get Envelope Certificate



```
GET https://connect.mindcloud.co/v1/universal/signPlus/latest/actions/get-envelope-certificate
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sign.Plus `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/signPlus/latest/actions/get-envelope-certificate?connectionId=$CONNECTION_ID&envelopeId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "envelopeId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/signPlus/latest/actions/get-envelope-certificate?${params}`, {
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
| `envelopeId` | string | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Sign.Plus API returns.

## Native endpoint

Through the native Sign.Plus API, this operation is `GET /envelope/:envelope_id/certificate` (base URL `https://restapi.sign.plus/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-envelope-certificate.md) for the provider-specific parameters and requirements.

