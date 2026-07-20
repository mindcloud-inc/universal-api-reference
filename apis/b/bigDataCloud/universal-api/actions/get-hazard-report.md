# BigDataCloud: Get Hazard Report

Retrieves hazard report details from BigDataCloud.

```
GET https://connect.mindcloud.co/v1/universal/bigDataCloud/latest/actions/get-hazard-report
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BigDataCloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bigDataCloud/latest/actions/get-hazard-report?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bigDataCloud/latest/actions/get-hazard-report?${params}`, {
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
| `ip` | string | no | If omitted, BigDataCloud uses the caller IP address. Example: `44.221.74.44`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "hostingLikelihood": 1,
      "iCloudPrivateRelay": true,
      "isBlacklistedBlocklistDe": true,
      "isBlacklistedUceprotect": true,
      "isBogon": true,
      "isCellular": true,
      "isHostingAsn": true,
      "isKnownAsMailServer": true,
      "isKnownAsProxy": true,
      "isKnownAsPublicRouter": true,
      "isKnownAsTorServer": true,
      "isKnownAsVpn": true,
      "isSpamhausAsnDrop": true,
      "isSpamhausDrop": true,
      "isSpamhausEdrop": true,
      "isUnreachable": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `hostingLikelihood` | number |  |
| `iCloudPrivateRelay` | boolean |  |
| `isBlacklistedBlocklistDe` | boolean |  |
| `isBlacklistedUceprotect` | boolean |  |
| `isBogon` | boolean |  |
| `isCellular` | boolean |  |
| `isHostingAsn` | boolean |  |
| `isKnownAsMailServer` | boolean |  |
| `isKnownAsProxy` | boolean |  |
| `isKnownAsPublicRouter` | boolean |  |
| `isKnownAsTorServer` | boolean |  |
| `isKnownAsVpn` | boolean |  |
| `isSpamhausAsnDrop` | boolean |  |
| `isSpamhausDrop` | boolean |  |
| `isSpamhausEdrop` | boolean |  |
| `isUnreachable` | boolean |  |

## Native endpoint

Through the native BigDataCloud API, this operation is `GET /data/hazard-report` (base URL `https://api-bdc.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-hazard-report.md) for the provider-specific parameters and requirements.

