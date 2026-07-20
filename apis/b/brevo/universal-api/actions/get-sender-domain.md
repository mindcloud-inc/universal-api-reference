# Brevo: Get Sender Domain



```
GET https://connect.mindcloud.co/v1/universal/brevo/latest/actions/get-sender-domain
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Brevo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/brevo/latest/actions/get-sender-domain?connectionId=$CONNECTION_ID&domainName=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "domainName": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/brevo/latest/actions/get-sender-domain?${params}`, {
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
| `domainName` | string | yes | The sender domain name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "domain": "string",
      "records": [
        {}
      ],
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `domain` | string | The sender domain. |
| `records` | array<object> | Domain DNS records. |
| `status` | string | The domain status. |

## Native endpoint

Through the native Brevo API, this operation is `GET /v3/senders/domains/:domainName` (base URL `https://api.brevo.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-sender-domain.md) for the provider-specific parameters and requirements.

