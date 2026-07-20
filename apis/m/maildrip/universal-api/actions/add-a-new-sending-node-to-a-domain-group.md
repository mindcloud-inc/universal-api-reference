# Maildrip: Add a new sending node to a domain group



```
POST https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/add-a-new-sending-node-to-a-domain-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Maildrip `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/add-a-new-sending-node-to-a-domain-group" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "userId": "string",
  "domainGroupId": "string",
  "nodeType": "string",
  "name": "Ava Chen",
  "host": "string",
  "port": 1,
  "username": "Ava Chen",
  "password": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/add-a-new-sending-node-to-a-domain-group', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "userId": "string",
    "domainGroupId": "string",
    "nodeType": "string",
    "name": "Ava Chen",
    "host": "string",
    "port": 1,
    "username": "Ava Chen",
    "password": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `userId` | string | yes | MongoDB User ID |
| `domainGroupId` | string | yes | Domain Group UUID |
| `nodeType` | string | yes |  |
| `name` | string | yes | Name for the sending node |
| `domainId` | string | no | Optional domain ID from Mumara |
| `replyTo` | string | no | Reply-to email address |
| `emailFrom` | string | no | From email display name/address |
| `status` | number | no | Node status (0=inactive, 1=active) |
| `host` | string | yes | SMTP host |
| `port` | number | yes | SMTP port |
| `username` | string | yes | SMTP username |
| `password` | string | yes | SMTP password |
| `encryptionMethod` | string | no | Encryption method |
| `mailEncoding` | string | no | Mail encoding |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |
| `success` | boolean |  |

## Native endpoint

Through the native Maildrip API, this operation is `POST /api/v1/mumara/sending-nodes` (base URL `https://api.maildrip.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-a-new-sending-node-to-a-domain-group.md) for the provider-specific parameters and requirements.

