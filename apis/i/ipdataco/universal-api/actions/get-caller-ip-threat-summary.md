# ipdata.co: Get Caller IP Threat Summary



```
GET https://connect.mindcloud.co/v1/universal/ipdataco/latest/actions/get-caller-ip-threat-summary
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ipdata.co `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ipdataco/latest/actions/get-caller-ip-threat-summary?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ipdataco/latest/actions/get-caller-ip-threat-summary?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "blocklists": [
        {}
      ],
      "isAnonymous": true,
      "isBogon": true,
      "isDatacenter": true,
      "isIcloudRelay": true,
      "isKnownAbuser": true,
      "isKnownAttacker": true,
      "isProxy": true,
      "isThreat": true,
      "isTor": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `blocklists` | array<object> | Blocklist matches for the caller IP. |
| `isAnonymous` | boolean | Whether the caller IP is anonymous. |
| `isBogon` | boolean | Whether the caller IP is a bogon. |
| `isDatacenter` | boolean | Whether the caller IP belongs to a datacenter. |
| `isIcloudRelay` | boolean | Whether the caller IP is an iCloud Private Relay address. |
| `isKnownAbuser` | boolean | Whether the caller IP is a known abuser. |
| `isKnownAttacker` | boolean | Whether the caller IP is a known attacker. |
| `isProxy` | boolean | Whether the caller IP is a proxy. |
| `isThreat` | boolean | Whether the caller IP is classified as a threat. |
| `isTor` | boolean | Whether the caller IP is a Tor exit node. |

## Native endpoint

Through the native ipdata.co API, this operation is `GET /threat` (base URL `https://api.ipdata.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-caller-ip-threat-summary.md) for the provider-specific parameters and requirements.

