# ironSource: Get Network Instances

Retrieves network instances from ironSource.

```
GET https://connect.mindcloud.co/v1/universal/ironSource/latest/actions/get-network-instances
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ironSource `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ironSource/latest/actions/get-network-instances?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ironSource/latest/actions/get-network-instances?${params}`, {
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
| `appKey` | string | no | Application key as seen on the LevelPlay platform. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "adFormat": "string",
      "adUnit": "string",
      "appConfig1": "string",
      "appConfig2": "string",
      "groups": [
        1
      ],
      "instanceConfig1": "string",
      "instanceConfig2": "string",
      "instanceId": "string",
      "instanceName": "Ava Chen",
      "isBidder": true,
      "isLive": true,
      "networkName": "Ava Chen",
      "rate": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `adFormat` | string | Ad format. |
| `adUnit` | string | Ad unit type per instance. |
| `appConfig1` | string | Network app-level configuration field. |
| `appConfig2` | string | Network app-level configuration field. |
| `groups` | array<number> | Mediation group IDs containing the instance. |
| `instanceConfig1` | string | Network instance-level configuration field. |
| `instanceConfig2` | string | Network instance-level configuration field. |
| `instanceId` | string | Unique network instance ID. |
| `instanceName` | string | Network instance name. |
| `isBidder` | boolean | Whether the instance is a bidder instance. |
| `isLive` | boolean | Whether the instance is active. |
| `networkName` | string | Ad network name. |
| `rate` | number | Instance-level rate when defined. |

## Native endpoint

Through the native ironSource API, this operation is `GET levelPlay/network/instances/v4/:appKey` (base URL `https://platform.ironsrc.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-network-instances.md) for the provider-specific parameters and requirements.

