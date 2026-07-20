# SparkPost: Create Sending Domain



```
POST https://connect.mindcloud.co/v1/universal/sparkPost/latest/actions/create-sending-domain
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SparkPost `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sparkPost/latest/actions/create-sending-domain" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "domain": "mail-codex-stage3-20260324.net"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sparkPost/latest/actions/create-sending-domain', {
  method: 'POST',
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
| `domain` | string | yes | Sending domain to create. Default: `mail-codex-stage3-20260324.net`. |
| `trackingDomain` | string | no | Associated tracking domain. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "dkim": {},
      "domain": "string",
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `dkim` | object |  |
| `domain` | string |  |
| `message` | string |  |

## Native endpoint

Through the native SparkPost API, this operation is `POST /sending-domains` (base URL `https://api.sparkpost.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-sending-domain.md) for the provider-specific parameters and requirements.

