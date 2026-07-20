# UpGuard: Retrieve Vendor IP Details

Retrieves details for a vendor IP address in UpGuard.

```
GET https://connect.mindcloud.co/v1/universal/upGuard/latest/actions/retrieve-vendor-ip-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a UpGuard `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/upGuard/latest/actions/retrieve-vendor-ip-details?connectionId=$CONNECTION_ID&vendorPrimaryHostname=Ava%20Chen&ip=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "vendorPrimaryHostname": "Ava Chen",
  "ip": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/upGuard/latest/actions/retrieve-vendor-ip-details?${params}`, {
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
| `vendorPrimaryHostname` | string | yes | The primary hostname of the vendor to show the IP detail for. |
| `ip` | string | yes | The IP address to retrieve details for. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "country": "string",
      "domains": [
        {
          "automatedScore": 1,
          "hostname": "Ava Chen"
        }
      ],
      "ip": "string",
      "owner": "string",
      "sources": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `country` | string |  |
| `domains[].automatedScore` | number |  |
| `domains[].hostname` | string |  |
| `ip` | string |  |
| `owner` | string |  |
| `sources[]` | string |  |

## Native endpoint

Through the native UpGuard API, this operation is `GET /vendor/ip` (base URL `https://cyber-risk.upguard.com/api/public`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-vendor-ip-details.md) for the provider-specific parameters and requirements.

