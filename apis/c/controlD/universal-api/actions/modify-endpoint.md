# Control D: Modify Endpoint

Updates an endpoint in Control D.

```
PUT https://connect.mindcloud.co/v1/universal/controlD/latest/actions/modify-endpoint
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Control D `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/controlD/latest/actions/modify-endpoint" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "deviceId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/controlD/latest/actions/modify-endpoint', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "deviceId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `deviceId` | string | yes | Device/Resolver ID |
| `name` | string | no | New Device name |
| `clientCount` | string | no | Number of devices using this Endpoint |
| `profileId` | string | no | Primary key of main profile to enforce on this device |
| `profileId2` | string | no | Primary key of a second profile to enforce -1 to remove. |
| `stats` | number | no | Set analytics level on device. 0 = off, 1 = basic, 2 = full |
| `legacyIpv4Status` | number | no | Set this to 1 to generate a legacy IPv4 (and IPv6) DNS resolver, 0 to remove existing one. |
| `learnIp` | number | no | Enable or disable automatic IP learning and logging. 0 to disable, 1 to enable. |
| `restricted` | number | no | Make this device restricted. 0 to disable, 1 to enable. |
| `bumpTls` | number | no | Enable or disable experimental ECH support and TLS bumping |
| `desc` | string | no | Add a description or comment to the device |
| `ddnsStatus` | number | no | Status of public DDNS endpoint. 1 = enabled, 0 = disable. |
| `ddnsSubdomain` | string | no | DDNS subdomain to expose the IP on |
| `ddnsExtHost` | string | no | DDNS hostname to query to learn new IPs |
| `ddnsExtStatus` | number | no | Status of DDNS based IP learning. 0 to disable, 1 to enable. |
| `status` | number | no | Update device status. 0 - pending, 1 - active, 2 - soft disabled, 3 - hard disabled |
| `ctrldCustomConfig` | string | no | ctrld .toml config file to deploy |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ddns": {},
      "ddns_ext": {},
      "desc": "string",
      "device_id": "string",
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
| `ddns` | object |  |
| `ddns_ext` | object |  |
| `desc` | string |  |
| `device_id` | string |  |
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

Through the native Control D API, this operation is `PUT /devices/:deviceId` (base URL `https://api.controld.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/modify-endpoint.md) for the provider-specific parameters and requirements.

