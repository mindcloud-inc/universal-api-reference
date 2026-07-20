# MailerSend: Get Domain Verification Status



```
GET https://connect.mindcloud.co/v1/universal/mailerSend/latest/actions/get-domain-verification-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MailerSend `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mailerSend/latest/actions/get-domain-verification-status?connectionId=$CONNECTION_ID&domainId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "domainId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mailerSend/latest/actions/get-domain-verification-status?${params}`, {
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
      "cname": true,
      "dkim": true,
      "mx": true,
      "rpCname": true,
      "spf": true,
      "tracking": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cname` | boolean |  |
| `dkim` | boolean |  |
| `mx` | boolean |  |
| `rpCname` | boolean |  |
| `spf` | boolean |  |
| `tracking` | boolean |  |

## Native endpoint

Through the native MailerSend API, this operation is `GET /domains/:domain_id/verify` (base URL `https://api.mailersend.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-domain-verification-status.md) for the provider-specific parameters and requirements.

