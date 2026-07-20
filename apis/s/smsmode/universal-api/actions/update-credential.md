# smsmode: Update Credential



```
PUT https://connect.mindcloud.co/v1/universal/smsmode/latest/actions/update-credential
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a smsmode `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/smsmode/latest/actions/update-credential" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "channelId": "string",
  "credentialId": "string",
  "type": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/smsmode/latest/actions/update-credential', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "channelId": "string",
    "credentialId": "string",
    "type": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `channelId` | string | yes | Channel ID path parameter from the smsmode API route. |
| `credentialId` | string | yes | Credential ID path parameter from the smsmode API route. |
| `name` | string | no | Name request body field documented by the smsmode API. |
| `type` | string | yes | Type request body field documented by the smsmode API. |
| `roles[]` | array | no | Roles request body field documented by the smsmode API. |
| `authorizedIps[]` | array | no | Authorized IPs request body field documented by the smsmode API. |
| `blocked` | boolean | no | Blocked request body field documented by the smsmode API. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "authorizedIps": [
        "string"
      ],
      "blocked": true,
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
| `blocked` | boolean |  |
| `name` | string |  |
| `roles[]` | string |  |
| `type` | string |  |

## Native endpoint

Through the native smsmode API, this operation is `PATCH commons/v1/channels/:channelId/credentials/:credentialId` (base URL `https://rest.smsmode.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-credential.md) for the provider-specific parameters and requirements.

