# UpGuard: List Vendor IPs

Retrieves IP addresses for a vendor in UpGuard.

```
GET https://connect.mindcloud.co/v1/universal/upGuard/latest/actions/list-vendor-ips
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a UpGuard `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/upGuard/latest/actions/list-vendor-ips?connectionId=$CONNECTION_ID&limit=25&offset=0&vendorPrimaryHostname=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "vendorPrimaryHostname": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/upGuard/latest/actions/list-vendor-ips?${params}`, {
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
| `vendorPrimaryHostname` | string | yes | The primary hostname of the vendor to list IPs for. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ips": [
        {
          "country": "string",
          "ip": "string",
          "owner": "string",
          "sources": [
            "string"
          ]
        }
      ],
      "nextPageToken": "string",
      "totalResults": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ips[].country` | string |  |
| `ips[].ip` | string |  |
| `ips[].owner` | string |  |
| `ips[].sources[]` | string |  |
| `nextPageToken` | string |  |
| `totalResults` | number |  |

## Native endpoint

Through the native UpGuard API, this operation is `GET /vendor/ips` (base URL `https://cyber-risk.upguard.com/api/public`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-vendor-ips.md) for the provider-specific parameters and requirements.

