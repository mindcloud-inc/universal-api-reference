# smsmode: Create Credential



```
POST https://connect.mindcloud.co/v1/universal/smsmode/latest/actions/create-credential
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a smsmode `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/smsmode/latest/actions/create-credential" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "channelId": "string",
  "name": "Ava Chen",
  "type": "string",
  "roles[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/smsmode/latest/actions/create-credential', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "channelId": "string",
    "name": "Ava Chen",
    "type": "string",
    "roles[]": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `channelId` | string | yes | Channel ID path parameter from the smsmode API route. |
| `name` | string | yes | Name request body field documented by the smsmode API. |
| `type` | string | yes | Type request body field documented by the smsmode API. |
| `roles[]` | array | yes | Roles request body field documented by the smsmode API. |
| `authorizedIps[]` | array | no | Authorized IPs request body field documented by the smsmode API. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "authorizedIps": [
        "string"
      ],
      "name": "Ava Chen",
      "roles": [
        "string"
      ],
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `authorizedIps[]` | string |  |
| `name` | string |  |
| `roles[]` | string |  |
| `type` | string |  |

## Native endpoint

Through the native smsmode API, this operation is `POST commons/v1/channels/:channelId/credentials` (base URL `https://rest.smsmode.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-credential.md) for the provider-specific parameters and requirements.

