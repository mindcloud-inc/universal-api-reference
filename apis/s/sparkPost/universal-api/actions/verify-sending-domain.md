# SparkPost: Verify Sending Domain



```
PUT https://connect.mindcloud.co/v1/universal/sparkPost/latest/actions/verify-sending-domain
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SparkPost `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/sparkPost/latest/actions/verify-sending-domain" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "domain": "mail-codex-stage3-20260324.net"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sparkPost/latest/actions/verify-sending-domain', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "domain": "mail-codex-stage3-20260324.net"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `cnameVerify` | boolean | no | Request CNAME verification. |
| `dkimVerify` | boolean | no | Request DKIM verification. |
| `domain` | string | yes | Sending domain to verify. Default: `mail-codex-stage3-20260324.net`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "abuseAtStatus": "string",
      "cnameStatus": "Ava Chen",
      "complianceStatus": "string",
      "dkimStatus": "string",
      "dns": {},
      "mxStatus": "string",
      "ownershipVerified": true,
      "postmasterAtStatus": "string",
      "spfStatus": "string",
      "verificationMailboxStatus": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `abuseAtStatus` | string |  |
| `cnameStatus` | string |  |
| `complianceStatus` | string |  |
| `dkimStatus` | string |  |
| `dns` | object |  |
| `mxStatus` | string |  |
| `ownershipVerified` | boolean |  |
| `postmasterAtStatus` | string |  |
| `spfStatus` | string |  |
| `verificationMailboxStatus` | string |  |

## Native endpoint

Through the native SparkPost API, this operation is `POST /sending-domains/:domain/verify` (base URL `https://api.sparkpost.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/verify-sending-domain.md) for the provider-specific parameters and requirements.

