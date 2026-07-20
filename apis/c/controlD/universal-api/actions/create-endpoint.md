# Control D: Create Endpoint

Creates an endpoint in Control D.

```
POST https://connect.mindcloud.co/v1/universal/controlD/latest/actions/create-endpoint
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Control D `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/controlD/latest/actions/create-endpoint" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "clientCount": "string",
  "profileId": "string",
  "icon": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/controlD/latest/actions/create-endpoint', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "clientCount": "string",
    "profileId": "string",
    "icon": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Device name |
| `clientCount` | string | yes | Number of devices using this Endpoint |
| `profileId` | string | yes | Primary key of main profile to enforce on this device |
| `profileId2` | string | no | Primary key of a second profile to enforce |
| `icon` | string | yes | Device icon/type |
| `stats` | number | no | Set analytics level on device. 0 = off, 1 = basic, 2 = full |
| `legacyIpv4Status` | number | no | Set this to 1 to generate a legacy IPv4 (and IPv6) DNS resolver. |
| `learnIp` | number | no | Enable or disable automatic IP learning and logging. 0 to disable, 1 to enable. |
| `restricted` | number | no | Make this device restricted, only previously authorized IPs will be able to query against it |
| `desc` | string | no | Add a description or comment to the device |
| `ddnsStatus` | number | no | Status of DDNS endpoint that exposes last used IP. |
| `ddnsSubdomain` | string | no | DDNS subdomain to expose the IP on |
| `ddnsExtStatus` | number | no | Status of DDNS based IP learning |
| `ddnsExtHost` | string | no | DDNS hostname to query to learn new IPs |
| `remapDeviceId` | string | no | Remap source device + client ID to a new device |
| `remapClientId` | string | no | Remap source device + client ID to a new device |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bump_tls": 1,
      "desc": "string",
      "device_id": "string",
      "icon": "string",
      "learn_ip": 1,
      "legacy_ipv4": {},
      "name": "Ava Chen",
      "PK": "string",
      "profile": {},
      "resolvers": {},
      "restricted": 1,
      "stats": 1,
      "status": 1,
      "ts": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bump_tls` | number |  |
| `desc` | string |  |
| `device_id` | string |  |
| `icon` | string |  |
| `learn_ip` | number |  |
| `legacy_ipv4` | object |  |
| `name` | string |  |
| `PK` | string |  |
| `profile` | object |  |
| `resolvers` | object |  |
| `restricted` | number |  |
| `stats` | number |  |
| `status` | number |  |
| `ts` | number |  |

## Native endpoint

Through the native Control D API, this operation is `POST /devices` (base URL `https://api.controld.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-endpoint.md) for the provider-specific parameters and requirements.

