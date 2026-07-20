# MailerSend: Get Domain DNS Records



```
GET https://connect.mindcloud.co/v1/universal/mailerSend/latest/actions/get-domain-dns-records
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MailerSend `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mailerSend/latest/actions/get-domain-dns-records?connectionId=$CONNECTION_ID&domainId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "domainId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mailerSend/latest/actions/get-domain-dns-records?${params}`, {
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
| `domainId` | string | yes | ID of the MailerSend domain. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "customTracking": {},
      "dkim": {},
      "id": "string",
      "inboundRouting": {},
      "returnPath": {},
      "spf": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `customTracking` | object |  |
| `dkim` | object |  |
| `id` | string |  |
| `inboundRouting` | object |  |
| `returnPath` | object |  |
| `spf` | object |  |

## Native endpoint

Through the native MailerSend API, this operation is `GET /domains/:domain_id/dns-records` (base URL `https://api.mailersend.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-domain-dns-records.md) for the provider-specific parameters and requirements.

