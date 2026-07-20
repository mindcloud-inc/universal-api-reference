# Control D: Modify Profile Service

Updates a profile service in Control D.

```
PUT https://connect.mindcloud.co/v1/universal/controlD/latest/actions/modify-profile-service
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Control D `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/controlD/latest/actions/modify-profile-service" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "profileId": "string",
  "service": "string",
  "do": 1,
  "status": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/controlD/latest/actions/modify-profile-service', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "profileId": "string",
    "service": "string",
    "do": 1,
    "status": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `profileId` | string | yes | Primary key (PK) of the profile |
| `service` | string | yes | Service name |
| `do` | number | yes | Rule type. 0 = BLOCK. 1 = BYPASS, 2 = SPOOF, 3 = REDIRECT. |
| `status` | number | yes | Rule status. 0 = disable. 1 = enabled |
| `via` | string | no | Spoof/Redirect target. If SPOOF, this can be an IPv4 or hostname. If REDIRECT, this must be a valid proxy identifier. <<glossary:Via>> |
| `viaV6` | string | no | If SPOOF this can be a valid IPv6 address (AAAA record) |

## Response

```json
{
  "success": true,
  "data": [
    {
      "do": 1,
      "status": 1,
      "via": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `do` | number |  |
| `status` | number |  |
| `via` | string |  |

## Native endpoint

Through the native Control D API, this operation is `PUT /profiles/:profileId/services/:service` (base URL `https://api.controld.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/modify-profile-service.md) for the provider-specific parameters and requirements.

