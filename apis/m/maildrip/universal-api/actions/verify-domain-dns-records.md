# Maildrip: Verify domain DNS records



```
GET https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/verify-domain-dns-records
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Maildrip `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/verify-domain-dns-records?connectionId=$CONNECTION_ID&domainId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "domainId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/verify-domain-dns-records?${params}`, {
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
| `domainId` | string | yes | Domain ID (DynamoDB UUID) |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "success": true,
      "verificationResults": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |
| `success` | boolean |  |
| `verificationResults` | object |  |

## Native endpoint

Through the native Maildrip API, this operation is `POST /api/v1/mumara/sending-domains/{domainId}/verify` (base URL `https://api.maildrip.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/verify-domain-dns-records.md) for the provider-specific parameters and requirements.

